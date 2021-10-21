# Dockers et Dockers Compose

## Dockers
Docker est une techologie permetant la création et la gestion de contenaire
Pour crée une container nous avons besoins d'un dockerFile.
Pour cette exemple nous allons utiliser HERO-API


### Dockerfile
Se fichier permet de décrire la construction d'un container. Il posséde plusieurs "command"

```dockerfile
#Base image
FROM python:3.9.6-alpine
```
FROM : nous permet de selectionner une image de base, dans notre cas nous allons partir du container "python" avec le tags "3.9.6-alpine"

```dockerfile
#Base image
WORKDIR /usr/src/app 
```
WORKDIR : nous permet de crée un dossier de travaille. 

```dockerfile
RUN apk update \
    && apk add postgresql-dev gcc python3-dev musl-dev
```
RUN : run execute des commande a l'intérieur du container pour installer ou configurer se que l'on souhaite. Dans notre cas il va installer les dépendance necessaire a l'utilsiation de postgresql.

```dockerfile
COPY requirements.txt /usr/src/app/requirements.txt

COPY herosite /usr/src/app/herosite
```
COPY : copie n'importe quelle fichier de la machine vers le container. Dans notre cas on copie le requirement.txt pour les dépendance python et l'application python.

```dockerfile
#allow tu run entrypoint
RUN chmod +x /usr/src/app/herosite/entrypoint.sh

#install python dependance
RUN pip install -r requirements.txt
```
On permet le lancement du script de lancement et on installe les dépendance python.



```dockerfile
ENTRYPOINT ["/usr/src/app/herosite/entrypoint.sh"]
```
ENTRYPOINT : définit la commande a lancer a l'entré dans le container 

Se qui nous donne donc pour se container :
```dockerfile
#Base image
FROM python:3.9.6-alpine

#Dossier de travaille
WORKDIR /usr/src/app 

#Update paquet and install postgre
RUN apk update \
    && apk add postgresql-dev gcc python3-dev musl-dev

COPY requirements.txt /usr/src/app/requirements.txt

COPY herosite /usr/src/app/herosite

#allow tu run entrypoint
RUN chmod +x /usr/src/app/herosite/entrypoint.sh

#install python dependance
RUN pip install -r requirements.txt

ENTRYPOINT ["/usr/src/app/herosite/entrypoint.sh"]
```



## Dockers-Compose