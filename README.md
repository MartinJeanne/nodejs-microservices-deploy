# Deploy

## How to deploy
Lauch the containers with:
```bash
docker compose up -d
```
- Then, connect to [Keycloak](http://localhost:8080/) with login and password: `root`
- Import the pre-made realm in: realm-export.json
- In the docker-compose.yml, in the environment variable "REALM_KEY" of the gateway service, put the RS256 key of you realm (on Keycloak, go to realm settings, and "keys" tab).
- Create an user named: martin
- Go to the created user, click the "Credential" tab, set the password (do not make it temporary) to be: martin
- Go to "Role mapping" tab, assign role "admin" to user.
- Restart containers to apply changes:
```bash
docker compose down
```
```bash
docker compose up -d --build
```

## Useful command
Rebuild the images, must be done if code of an app changed
docker compose up -d --build

Delete existing infra + delete volumes
docker compose down -v

Delete unsed images
docker image prune -a
