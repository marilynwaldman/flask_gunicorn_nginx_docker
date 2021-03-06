

### This was adapted from :
https://towardsdatascience.com/how-to-deploy-ml-models-using-flask-gunicorn-nginx-docker-9b32055b3d0

This app is composed of three modules:

1.  get_maps.py : Downloads .html files from maps from Google Drive.  The files are zip files for each map.

2.  app.py : A small flask server serving the .html maps downloaded from the above.  This app was adapted from:  https://github.com/gotoariel/folium-demo

3.  ngnix : nginx will be the reverse proxy and ingress.

To run clone the repo, cd to the directory and execute:

```
sudo bash run_docker.sh
```


**************************************************


****************************************************

# Template for deploying ML models using Flask + Gunicorn + Nginx inside Docker

## Running the solution

In order to run this solution, you just have to install Docker, Docker compose, then clone this repository, and then:
```
bash run_docker.sh
```

# flask_gunicorn_nginx_docker
Template for deploying ML models using Flask + Gunicorn + Nginx inside Docker


For Docker installation instructions follow:

— [Docker installation](https://docs.docker.com/engine/install/ubuntu/)

— [Make Docker run without root](https://docs.docker.com/engine/install/linux-postinstall/)

— [Docker Compose installation](https://docs.docker.com/compose/install/)

## Understanding the solution

— The detailed way: check [my Medium post](https://towardsdatascience.com/how-to-deploy-ml-models-using-flask-gunicorn-nginx-docker-9b32055b3d0) regarding this solution. 

— The fast way: the project is structured as follows: Flask app and WSGI entry point are localed in flask_app directory. Nginx and project configuration files are located in nginx directory. Both directories contain Docker files that are connected using docker_compose.yml file in the main directory. 
  
   For simplicity, I also added run_docker.sh file for an even easier setting-up and running this solution. 
```
.
├── flask_app 
│   ├── app.py          
│   ├── wsgi.py
│   └── Dockerfile
├── nginx
│   ├── nginx.conf          
│   ├── project.conf
│   └── Dockerfile
├── docker-compose.yml
└── run_docker.sh
```
