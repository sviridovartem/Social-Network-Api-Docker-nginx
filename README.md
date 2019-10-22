# Social-Network-Api-Docker-nginx
## Description
For production environments, we use Nginx and Gunicorn.
Main pages:
1. `/admin/`
2. `/friendship/`
3. `/group/`
4. `/news/`
5. `/subscription/`
## How to run
Dev version:
1. Build the image: `$ docker-compose build`
2. Run the container: `$ docker-compose up -d`

To see result Navigate to `http://localhost:8000/`.

Prod version:
1. Build  and run image: 
`$ docker-compose -f docker-compose.prod.yml up -d --build`
2. Make migrations: 
`$ docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput`

To see result Navigate to `http://localhost:1337/`.

To stop container:
1. Prod:
`$ docker-compose -f docker-compose.prod.yml down -v`
2. Dev:
`docker-compose down -v`



