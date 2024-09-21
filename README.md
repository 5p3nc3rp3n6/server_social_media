# 
docker build -t server_social_media .
docker build -t kaipus/server_social_media:2.0.0 .
docker buildx build --platform linux/amd64 -t kaipus/server_social_media:1.0.0 .
docker push kaipus/server_social_media:2.0.0

docker run -dp 8081:2999 server_social_media
