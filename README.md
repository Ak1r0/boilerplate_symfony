# Boilerplate for symfony with postgre Database and caddy server

## Versions

### Defaults

- PHP : 8.2.* 
- Symfony : stable 
- Caddy : 2.6
- Composer : 2
- Postgre : Alpine 15

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
