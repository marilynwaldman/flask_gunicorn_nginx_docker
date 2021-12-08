# flask_gunicorn_nginx_docker
Template for deploying ML models using Flask + Gunicorn + Nginx inside Docker

### This was adapted from :
https://towardsdatascience.com/how-to-deploy-ml-models-using-flask-gunicorn-nginx-docker-9b32055b3d0

This app is composed of three modules:

1.  get_maps.py : Downloads .html files from maps from Google Drive.  The files are zip files for each map.

2.  app.py : A small flask server serving the .html maps downloaded from the above.  This app was adapted from:  https://github.com/gotoariel/folium-demo

3.  ngnix : nginx will be the reverse proxy and ingress.



