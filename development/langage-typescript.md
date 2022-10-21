# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'intéret de TypeScript dans l'IDE  ✔️
il permet d'eviter les erreurs d'ortographes et d'etre sur de recevoir/afficher le bon type de données

- les types de bases  ✔️
The primitives : string, number and boolean

- comment et pourquoi étendre une interface  ✔️
les interface ne fonctionne que dans leur page il faut donc les exporter pour povoir les utlisier dans dautre pages et ne pas avoir a repeter de code.

- les classes et les decorators ❌ / ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️
 ````typescript

// interfaces

export interface IWilder { // declaration de l'interface et exportation
  id: number;               // propriété et son type
  name: string;
  upvotes: IUpvote[];      // ici le type est un tableau d'une autre interface
}
export interface IUpvote {
  id: number;
  upvotes: number;
  skill: ISkill;     // ici on represente la relation entre nos entités
  wilder: IWilder;    // en y ajoutant un type de l'entité lié
}


// fetching data from DB

function App() {
  const [wilders, setWilders] = useState<IWilder[]>([]); // ici on "type" le usestate en utlisant un generic ce qui permet a la function de recevoir des données de tout les types present dans IWilder

  const fetchData = async (): Promise<void> => { 
    // ici la fuonction est de type async await elle retourne donc une promesse vide on la type donc en Promise<void>
    const wilders = await axios.get("http://localhost:5000/api/wilders");
    setWilders(wilders.data);
  };

  useEffect((): void => { // fonction qui ne fait pas de retour : "void"
    fetchData();
  }, []);
````

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
