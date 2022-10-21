# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- Comment développer en utilisant un système de *livereloading* (`nodemon` par exemple)  ✔️

  Live reload is an automated approach to restarting our application during development. It enables our app to automatically and simultaneously pick up code changes while we are coding. Enabling this saves you countless manual and tedious restarts.

- La connexion de mon application à une base de données avec et sans ORM/ODM (avec `mongodb` puis `mongoose` par exemple)  ✔️

- Le développement d'une API REST et GraphQL (avec les packages `express` et `graphql` par exemple)  ✔️

- *Bonus : la manipulation des fichiers système avec `fs` et l'utilisation des streams en NodeJS* ❌ 

## 💻 J'utilise

### Un exemple personnel commenté ❌ / ✔️

```typescript
//  EX 1 : connection a DB SQLITE
import { DataSource } from "typeorm";
import { Skill } from "./entities/Skill";
import { Upvote } from "./entities/Upvote";
import { Wilder } from "./entities/Wilder";

const datasource = new DataSource({      <- connexion a Database  avec orm
  type: "sqlite",
  database: "./wilders.db",
  synchronize: true,
  entities: [Wilder, Skill, Upvote],
  logging: ["query", "error"],
});
export default datasource;
```

```typescript
// EX 2 :  Une entitée

import { Entity, Column, PrimaryGeneratedColumn, ManyToOne } from "typeorm";
import { Skill } from "./Skill";
import { Wilder } from "./Wilder";

@Entity() // declaration de l'entité
export class Upvote {
  @PrimaryGeneratedColumn() // premierer colonne : id autogenerer
  id: number;  // nom et typage en Ts

  @Column({ default: 0 }) // ici ajout d'un nombre par defaut
  upvotes: number;

  @ManyToOne(() => Skill, "upvotes") // relation avec l'entité Skill
  skill: Skill;

  @ManyToOne(() => Wilder, "upvotes", { onDelete: "CASCADE" }) 
  // ajout de la suppresion en cascade lors de la suppresion d'un wilder
  wilder: Wilder;
}
````


// ```javascript
// // this function takes a path to a .md file of the host system and write the HTML version of this file
// // the .html file is given back
// const convertMDFileToHTML = (pathToMDfile) => /* ... path to HTML file */
// ```

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
