# Geovillage
> Community driven delivery platform for the ones who need it the most

## Installation Instructions

1. **Install PostgreSQL and PostGIS**
Docker installation:
    - Install [Docker](https://docs.docker.com/get-docker/)
    - Download and run the official [PosgreSQL/PostGIS docker image](https://registry.hub.docker.com/r/postgis/postgis/)

2. **Install `python3.7` and `pip3`**

3. **Install Homebrew and these dependencies**
   - brew install postgresql
   - brew install postgis
   - brew install gdal
   - brew install libgeoip

4. **Create a python virtual environment using `venv`**
    `python3 -m venv ~/python-virtual-environments/geovillage`

5. **Activate virtual environment**
    `source ~/python-virtual-environments/geovillage/bin/activate`

6. **Install Django and other dependencies**
    - pip install django==3.0.6
    - pip install psycopg2==2.8.5
    - pip install djangorestframework==3.11.0
    - pip install django-environ==0.4.5

## Instructions to run

1. **Start PostgreSQL database service**
    If you installed via docker, run `docker run --name geovillage-postgis -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgis/postgis`

2. **Start Django web server (Make sure the virtual environment is activated)**
    `python3 manage.py runserver`

## To write psql queries
1. SSH into your Postgres docker container: `docker exec --user postgres -it geovillage-postgis /bin/bash` 
2. Run `psql` on the terminal
