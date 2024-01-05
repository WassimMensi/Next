# Notes Autres
Dom = Document Object Model est une interface de programmation normalisée par le W3C, qui permet à des scripts d'examiner et de modifier le contenu du navigateur web.  
Dans le dev Js (react ou next) on a tendance à utiliser comme page principale une page "index" en html, c'est celle qui est affiché en permanence.  
On appel ce type d'application des "SPA"(Single-page application) car tout ce passe dans une seule page web, tout est simulé par la partie JS pour limiter les intéractions avec le serveur, l'inconvénient principal est que c'est le navigateur qui va se charger de tout(l'app peut donc consommer beaucoup de RAM).  
Lighthouse : plugin pour connaitre le référencement d'un site.  
Le TypeScript est une surcouche de JavaScript qui permet de typer les variables, cela rend le Js moins "libre" et plus encadré (utile uniquement pour le développeur, le client n'est pas impacté par le Ts).  
Outils autres : chadCN & Tailwind(css) & AG Grid(tab compatible avec react/js)  
jsx + ts = tsx  
rout = Next.js uses a file-system based router where folders are used to define routes.  
Each folder represents a route segment that maps to a URL segment. To create a nested route, you can nest folders inside each other.  
app correspond à / et dashboard correspond donc à /dashboard.  
![Cours](routes.png "Schéma")  

# Partie React

## Intro
React est une bibliothèque JavaScript libre. Elle est maintenue par Meta ainsi que par une communauté de développeurs individuels et d'entreprises depuis 2013.

## Installation
npm create vite@latest my-react-app --template react  
cd my-react-app  
npm install  
npm run dev  

Vite sert a mettre en place son application, rapide et performant, il sert à faciliter le travail avec react.

### Infos et Voc Part-1
En react tous les composants sont des fonctions.  
Un composant est donc une fonction qui return du JSX.  
En React "<>" permet de rendre le DOM plus lisible.  
React mets à jour le DOM avec les hooks.
Hook permet de gérer l'état et le cycle de vie des rendues.  
Ce sont des fonctions qui commencent par use (convention).  
On peut utiliser une fonction pour mettre a jour le states.  
Cette syntaxe "setName((prev)=>{return prev + "vite";})" est utile quand on veut mettre un state dont la valeur depend de la valeur précédente.  
Les composants React communiquent entre eux avec des props.  
Tous les composants peuvent recevoir en parametre des props. 
Ce sont des objets dont l'utilisation est similaire a celle des attributs html.  
Les props sont utile lorsqu'on veut passer d'enfant à parents, au dela ils deviennent dépassés.  
La props "children" est présente dans tous les ocmposants de base.  

# Consignes TP React

## Partie 1
- [ ] Créer un nouveau projet React avec vite
- [ ] Créer un composant `App`
- [ ] Créer un composant `Header`
- [ ] Créer un composant `Footer`
- [ ] Créer un composant `Main` qui affiche un profil utilisateur
- [ ] Utilisez un formulaire dont l'affichage est conditionné par un bouton
- [ ] Le fromulaire doit permettre de modifier le profil utilisateur
- [ ] utilisez les modules CSS
- [ ] Utilisez les props
- [ ] Utilisez les states
- [ ] L'application doit etre responsive (mobile first)
// il me reste a rendre responsive l'app

## Partie 2
- [ ] Creer un nouveau projet React avec Vite
- [ ] Cette fois ci l'application permettra de gerer les elements d'une liste a l'aide d'un formulaire
- [ ] Créer un composant `List` qui affiche une liste de profil utilisateur
- [ ] Creer un formulaire qui permet d'ajouter un profil utilisateur à la liste
- [ ] Trouvez un moyen de filtrer la liste des profils par annee de naissance par exemple  
(tester useeffect, usecontext et api context.)  
(utiliser useReducer au lieu de useState.)  

### Infos et Voc Part-2
Useeffect : fait en sorte que quelquechose qui ne provient pas de react marche dans react.  
Utilité : placer tout ses "sideEffects".  
Systeme de login pour ne pas utiliser un systeme de props. 
Hook : fonction mis a disposition part la bibliotheque react qui permet de gérer les cycles de vies de composants react.
L'etat est géré par le hook.  
Reducer: The reducer function that specifies how the state gets updated. It must be pure, should take the state and action as arguments, and should return the next state. State and action can be of any types.  
HookUseReducer permet de récupérer le state dans sa version la plus récente.  
API context permet de partager une fonction reducer ou une variable dans toute l'application.  
-context provider = composant react  
-props.children -> a way to pass the state data to a component as the props  
Donc au lieu de state et useState utiliser plutot state et dispatch afin de rendre disponible un reducer ou une variable dans toute l'app.  
### Schéma :  
![Cours](store.png "Schéma")  

# Partie Next

## Intro
Next est un framework React qui permet de créer des applications Web.  
Le framework se charge d'apporter tous les outils de bunling, compilation et bien plus...  
Next utilise des composants react pour l'interface et apporte de l'optimisation pour le referencement ainsi qu'en performance.  
Next est open source (accessible sur gitHub).

## Principales fonctionnalités

Next.js est un framework pour React, conçu pour la production et l'efficacité. Il offre plusieurs avantages :

**Server-Side Rendering (SSR)** : Next.js permet le rendu côté serveur des pages web, ce qui améliore la performance et le SEO.
**Static Site Generation (SSG)** : Possibilité de générer des sites statiques pour une vitesse de chargement rapide.
Routing Automatique : Les fichiers dans le dossier pages deviennent automatiquement des routes.
**Optimisation des Performances** : Next.js inclut des fonctionnalités comme l'optimisation automatique des images.
Facilité de Déploiement : Intégration simple avec des plateformes comme Vercel pour un déploiement rapide.

## Installation

Pour installer Next.js, vous pouvez utiliser `npx create-next-app` ou `yarn create next-app`. Vous pouvez aussi utiliser `npm init next-app` ou `yarn create next-app` pour créer un projet Next.js à partir de zéro.

Pour ce cours, nous allons utiliser `npx create-next-app` pour créer un projet Next.js à partir d'un template. Pour cela, exécutez la commande suivante dans votre terminal :

```bash

npx create-next-app --example with-tailwindcss nextjs-course

```

Cette commande va créer un nouveau dossier nextjs-course avec un projet Next.js préconfiguré avec Tailwind CSS. Vous pouvez ensuite ouvrir le dossier dans votre éditeur de code favori.

Pour lancer le projet, exécutez la commande suivante :

```bash

cd nextjs-course
npm run dev

```

Vous pouvez ensuite ouvrir http://localhost:3000 pour voir le résultat.

# Consignes TP Next

## Partie 1 - Tutoriel
Suivre le tuto : https://nextjs.org/learn/dashboard-app  
https://nextjs.org/learn/dashboard-app/error-handling (j'en suis au chapitre 13)

### Infos et Voc Part-1
Tout ce qui est destiné a etre une page -> dans le dossier app  
En général on place dans le layout les parties static de l'app(header+footer)  
--> créé a l'exterieur du dossier app (par exemple dans un dossier Ui)  
CLSX -> mise en forme conditionnel.  
Les composants next sont coté serveur, la directive "useClient" indique un composant comme "client".  
C'est une bonne chose de comprendre le système de Loading et des squellettes si l'ont souhaite faire du React.  

## Routing de Base avec Next.js

Le routing de base avec Next.js est très simple. Il suffit de créer un fichier dans le dossier pages avec le nom de la route. Par exemple, pour créer une page à l'adresse `/about`, il suffit de créer un fichier `about.js` dans le dossier pages.

![Alt text](image.png)

Vocabulaire du systeme de routing de Next.js :

- **Tree** (arbre): Un arbre est une structure de données qui représente une hiérarchie. Dans Next.js, l'arborescence des fichiers dans le dossier pages représente l'arborescence des routes.
- **Subtree**: Un sous-arbre est un arbre qui fait partie d'un arbre plus grand. Dans Next.js, un sous-arbre est un dossier qui fait partie de l'arborescence des fichiers dans le dossier pages.
- **Root**: La racine est le dossier le plus haut dans l'arborescence des fichiers. Dans Next.js, le dossier pages est la racine de l'arborescence des fichiers.
- **Leaf**: Une feuille est un nœud qui n'a pas d'enfants. Dans Next.js, un fichier dans le dossier pages est une feuille.

La presence du dossier pages est obligatoire dans un projet Next.js. Si vous supprimez ce dossier, vous empecher le bon fonctionnement du router.

Par defaut tous les composants situes dans le dossier app sont des `React Server Components`.

En resumé:

- Les dossiers permettent de definir les routes
- Les fichiers permettent de representer l'ui

Il existe tout un systeme de nomenclature des fichiers et de conventions afin d'assurer le bon fonctionnement du router:

- **layout**: permet de definir une UI commune pour plusieurs pages
- **page**: l'ui qui correspond a une route unique
- **loading**: la page de chargement commune a un segment et ses enfants
- **error**: ui en cas d'erreur
- **not-found**: ui lorsque la page n'est pas trouvee

### Navigation entre les pages

Il existe deux facons de naviguer entre les pages dans Next.js :

- Le composant **Link**: permet de naviguer entre les pages sans recharger la page:

```ts
import Link from "next/link";

export default function Page() {
  return (
    <div>
      <Link href="/about">
        <a>About</a>
      </Link>
    </div>
  );
}
```

Link est un composant fourni par Next.

- **Le hook useRouter**: permet de naviguer depuis un composant client par le code (l'usage de hook requiert l'urilisation de la directive 'use client')

Il existe un hook tres utile qui permet de verifier quel est le chemin actuel de l'application: usePathname

```ts
import { usePathname } from "next/router";

export default function Page() {
  const pathname = usePathname();
  return <div>Current path: {pathname}</div>;
}
```