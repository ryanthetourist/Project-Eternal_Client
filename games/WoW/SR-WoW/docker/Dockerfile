# Serves the built web client (publish/) with nginx. Build the project first (scons ... ), then from games/WoW/SR-WoW:
#   docker build -f docker/Dockerfile -t wow-eternal .
#   docker run -d -p 8080:8080 --name wow-eternal wow-eternal
# The game's own files are NOT in the image: the page reads them from a folder chosen in the browser (or mount them, see README).
FROM nginx:1.27-alpine
COPY docker/nginx.conf /etc/nginx/conf.d/default.conf
COPY publish/ /usr/share/nginx/html/
EXPOSE 8080
