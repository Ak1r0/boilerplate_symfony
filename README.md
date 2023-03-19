# Boilerplate for symfony with postgre Database and caddy server

Based on [dunglas/symfony-docker](https://github.com/dunglas/symfony-docker)

## Versions

### Defaults

- PHP : 8.2.* 
- Symfony : stable 
- Caddy : 2.6
- Composer : 2
- Postgre : 15

### Custom

Use [docker environnement attribute](https://docs.docker.com/compose/environment-variables/set-environment-variables/#substitute-from-the-shell) to change versions

`POSTGRES_VERSION=14; make build`

Availabe env vars :

```
      Name                            Default                         Desciption

SYMFONY_VERSION             6.2        
STABILITY                   stable                                 Symfony stability
POSTGRES_VERSION            15         
POSTGRES_USER               app
POSTGRES_PASSWORD           !ChangeMe!
POSTGRES_DB                 app
CADDY_MERCURE_JWT_SECRET    !ChangeThisMercureHubJWTSecretKey!
MERCURE_SUBSCRIBER_JWT_KEY  !ChangeThisMercureHubJWTSecretKey!
HTTP_PORT                   80
HTTPS_PORT                  443

```

## Shorcuts (with make)

```sh
 —— 🎵 🐳 The Symfony Docker Makefile 🐳 🎵 ——————————————————————————————————
help                           Outputs this help screen
 —— Docker 🐳 ————————————————————————————————————————————————————————————————
build                          Builds the Docker images
up                             Start the docker hub in detached mode (no logs)
start                          Build and start the containers
down                           Stop the docker hub
logs                           Show live logs
sh                             Connect to the PHP FPM container
 —— Composer 🧙 ——————————————————————————————————————————————————————————————
composer                       Run composer, pass the parameter "c=" to run a given command, example: make composer c='req symfony/orm-pack'
vendor                         Install vendors according to the current composer.lock file
 —— Symfony 🎵 ———————————————————————————————————————————————————————————————
sf                             List all Symfony commands or pass the parameter "c=" to run a given command, example: make sf c=about
cc                             Clear the cache
```
