# docker-compose-traefik-1.7


Empty the acme.json file then run docker-compose up.
Run docker network create traefik-net

    labels:
      - "traefik.docker.network=traefik-net"
      - "traefik.enable=true"
      - "traefik.basic.frontend.rule=Host:drive.spgo.xyz"
      - "traefik.basic.port=80"
      - "traefik.basic.protocol=http"

networks:
  internal:
  traefik-net:
    external: true
