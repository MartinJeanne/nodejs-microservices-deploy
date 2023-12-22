Usefull Docker commands:

Rebuild the images, must be done if code of an app changed
docker compose up -d --build

Delete existing infra + delete volumes
docker compose down -v

Delete unsed images
docker image prune -a
