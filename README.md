# Deploy

## How to deploy
Lauch the containers with:
```bash
docker compose up -d
```
Then, import the pre-made realm in [Keycloak](http://localhost:8080/) with: realm-export.json

Then check the Gateway README.md

## Useful command
Usefull Docker commands:

Rebuild the images, must be done if code of an app changed
docker compose up -d --build

Delete existing infra + delete volumes
docker compose down -v

Delete unsed images
docker image prune -a
