# GraphQL

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- la différence entre REST et GraphQL  ✔️

    L’élément pivot de REST est la ressource. Une API REST comprend un endpoint propre à chaque ressource, avec des méthodes de requêtes HTTP différentes. Si on prend exemple sur l’API d’un blog, avec deux ressources, l’une pour les auteurs, l’autre pour les articles.

    GraphQl a été pensé pour pouvoir condenser les multiples requêtes de REST en une seule, elle est donc optimisée pour l’échange de grands paquets de données et permettre des temps de réponse plus court dans ce genre de cas, mais surtout limiter les cas d’over-fetching ou d’under-fetching.

- les besoins auxquels répond GraphQL  ✔️

    permet aux développeurs de créer des requêtes qui extraient les données de plusieurs sources à l'aide d'un seul appel d'API, et les équipes chargées de la maintenance des API peuvent librement ajouter ou retirer des champs sans perturber les requêtes existantes.

- la définition d'un schéma ✔️

    A GraphQL schema is a description of the data clients can request from a GraphQL API. It also defines the queries and mutation functions that the client can use to read and write data from the GraphQL server

- Query  ✔️

     query is used to read or fetch values, the operation is a simple string that a GraphQL server can parse and respond to with data in a specific format.

- Mutation  ✔️

    A GraphQL mutation is used to write or post values, the operation is a simple string that a GraphQL server can parse and respond to with data in a specific format.

- Subscription ❌ 

 Subscriptions are a GraphQL feature that allows a server to send data to its clients when a specific event happens. Subscriptions are usually implemented with WebSockets. In that setup, the server maintains a steady connection to its subscribed client.

## 💻 J'utilise

### Un exemple personnel commenté  ✔️

exemple d'un schema en typegraphQl:
<!-- 
import { Entity, Column, PrimaryGeneratedColumn, OneToMany } from "typeorm";
import { Upvote } from "./Upvote";
import { ObjectType, Field, ID, InputType } from "type-graphql";
import { Length, IsIn } from "class-validator"; <- on utilise les class validator pour valider les données avant qu'elle ne soit ajouter a la bdd

@Entity()
@ObjectType()       <-@ObjectType decorator. It marks the class as the type known from the GraphQL.
export class Wilder {
  @PrimaryGeneratedColumn()
  @Field(() => ID)  <- we declare which class properties should be mapped to the GraphQL fields.For simple types (like string or boolean) this is all that's needed but due to a limitation in TypeScript's reflection, we need to provide info about generic types (like Array or Promise). So to declare the Rate[] type, we have to use the explicit [ ] syntax for array types - @Field(type => [Rate])
  id: number;

  @Column()
  @Field()
  name: string;

  @Column()
  @Field()
  city: string;

  @Column({ nullable: true })
  @Field({ nullable: true })
  age: number;

  @OneToMany(() => Upvote, "wilder")
  @Field(() => [Upvote])
  upvotes: Upvote[];
}
} -->


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
https://graphql.org/learn/
https://typegraphql.com/docs/introduction.html
- description
documentation officiel

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
