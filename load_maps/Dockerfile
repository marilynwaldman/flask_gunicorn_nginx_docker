FROM python:3.9
#docker build -t load_maps .
#docker volume create static
#docker run -v static:/static load_maps .
#docker run -v temp-vol alexf/myapp .
#docker inspect -f static *.html

#removecontainers() {
#docker stop $(docker ps -aq)
#docker rm $(docker ps -aq)

COPY . .
RUN pip install --no-cache-dir -r requirements.txt
# define the port number the container should expose
CMD [ "python", "./get_maps.py"]
