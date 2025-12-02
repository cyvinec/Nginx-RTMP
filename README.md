# Nginx-RTMP
Docker container of Nginx-RTMP

Default Nginx settings
----------------------
docker run --rm -d -p 80:80 ghcr.io/cyvinec/nginx

Multi Sites with RTMP Server
----------------------------
docker run --rm -d -p 80:80 \
-v ./volumes/nginx/conf.d:/etc/nginx/conf.d \
-v ./volumes/nginx/nginx.conf:/etc/nginx/nginx.conf \
-v ./volumes/www/site1:/var/www/html \
ghcr.io/cyvinec/nginx
