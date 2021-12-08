FROM python:3.9
#docker-compose down
#docker rm -f $(docker ps -a -q)
#docker volume rm $(docker volume ls -q)
#docker build -t load_maps .
#docker volume create static
#docker run -v app:/app load_maps .
#docker run -v temp-vol alexf/myapp .
#docker inspect -f app *.html
#--mount source=nginx-config,target=/etc/nginx \
#docker volume create --name static_maps
#docker run -t -i -v static_maps:/app/static load_maps /bin/bash
#docker run -t -i -v static:/app/static load_maps /bin/bash
#docker volume inspect [OPTIONS] VOLUME [VOLUME...]
#docker volume inspect static_maps

#removecontainers() {
#docker stop $(docker ps -aq)
#docker rm $(docker ps -aq)
WORKDIR /app
COPY . .
RUN pip install --no-cache-dir -r requirements.txt
# define the port number the container should expose

#CMD [ "python", "get_maps.py"]
