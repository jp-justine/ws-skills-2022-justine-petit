# Docker

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- la création d'une image docker  ✔️

    creation d'un dockerfile exemple : 
    "FROM node:alpine

    WORKDIR /app

    COPY package.json  package.json 
    COPY package-lock.json  package-lock.json 
    RUN npm i

    COPY  src  src
    COPY tsconfig.json tsconfig.json

    CMD npm start"

    puis lancement avec la commande " docker build -t <nom de l'image souhaiter> . "
    L’argument -t permet de spécifier un tag à notre image.


- l'éxécution d'un container  ✔️
    utilisation de la commande :
    " docker run <nom de l'image>" 
    ou avec options:
    "docker run [OPTIONS] IMAGE [COMMAND] [ARG...]"


- l'orchestration de containers avec docker-compose  ✔️

    Docker compose est une fonctionnalité permettant d'orchestrer plusieurs conteneurs qui doivent travailler ensemble. Pour ce faire, on crée un fichier YAML (Yet Another Markup Language) à l'intérieur duquel on spécifie les configurations nécessaires à chaque service


## 💻 J'utilise

### Un exemple personnel commenté ✔️
// docker-compose.yml

        version: '3'  <- L'argument version permet de spécifier à Docker Compose quelle version on  souhaite utiliser, et donc d'utiliser ou pas certaines versions. Dans notre cas, nous utiliserons la version 3, qui est actuellement la version la plus utilisée.>

    services: <- les conteneurs à exécuter ici api et db>
    api:
        build:  ./   <-argument build, en lui spécifiant le chemin vers notre fichier Dockerfile,permet lors de l’exécution de Docker Compose,de construire  un conteneur via le Dockerfile avant de l’exécuter.>
        ports:  <-argument, ports  , permet de dire à Docker Compose qu'on veut exposer un port de notre machine hôte vers notre conteneur, et ainsi le rendre accessible depuis l'extérieur.>
        - 3000:5000
        volumes:    <-Définissez le volume pour faire persister vos données>
        - ./src:/app/src
    db:
        image: postgres  <-permet de définir l'image Docker que nous souhaitons utiliser>
        environment:   <-L'image MySQL fournie dispose de plusieurs variables d'environnement que vous pouvez utiliser ; dans votre cas, nous allons donner au conteneur les valeurs des différents mots de passe et utilisateurs qui doivent exister sur cette base.>
        POSTGRES_PASSWORD: supersecret

### Utilisation dans un projet ❌ / ✔️

[lien github](...)

Description :

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

- lien
- description

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
