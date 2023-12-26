# Deploy

## How to deploy
Lauch the containers with:
```bash
docker compose up -d
```
Then, import in [Keycloak](http://localhost:8080/) the pre-made realm with: realm-export.json
Keycloak login and password are: `root`

In the docker-compose.yml, in the environment variable "REALM_KEY" of the gateway service, put the RS256 key of you realm (on Keycloak, go to realm settings, and "keys" tab).
Create an user named: martin
Go to the created user, click the "Credential" tab, set the password (do not make it temporary): martin
Go to "Role mapping" tab, assign role "admin" to user.

## Useful command
Usefull Docker commands:

Rebuild the images, must be done if code of an app changed
docker compose up -d --build

Delete existing infra + delete volumes
docker compose down -v

Delete unsed images
docker image prune -a
