# Deploy

## How to deploy
Lauch the containers with:
```bash
docker compose up -d
```
Then, import in [Keycloak](http://localhost:8080/) the pre-made realm with: realm-export.json
Keycloak login and password are: `root`

Then check the Gateway README.md

## Useful command
Usefull Docker commands:

Rebuild the images, must be done if code of an app changed
docker compose up -d --build

Delete existing infra + delete volumes
docker compose down -v

Delete unsed images
docker image prune -a
