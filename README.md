# CONFIG
- php 8.0.9
- mysql
- phpmyadmin
- mercure

# API

- Documentation url : https://127.0.0.1:8000/api
- Collection : Recipe
- Method Allow : POST, GET, PUT, DELETE, PATH
- Ressource URL : /api/recipes

```
"hydra:member": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "id": 0,
      "title": "string"
    }
```

# GET STARTED

Install dependencies
```
composer install
```
Mount Docker containers
```
docker-compose up -d
```
Load migrations to create tables mysql 
```
php ./bin/console doctrine:migrations:migrate
```
With CLI
```
symfony console doctrine:migrations:migrate
```
Start server
```
php -S 127.0.0.1:8000 -t public
```
With CLI
```
symfony serve
```

Controller page :
> https://127.0.0.1:8000/recipe/new

# Postman request

### URL : http://127.0.0.1:8000/api/recipes
### Methode : POST
### Body : JSON
```
{
    "title": "FROM POSTMAN"
}
```

# KILL CONTAINERS
```
docker-compose down
docker-compose down --remove-orphans
```
# CLEAN VOLUMES
```
docker volume rm $(docker volume ls -q)
```

