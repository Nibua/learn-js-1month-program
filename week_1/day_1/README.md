## Day 1: Introduction to JavaScript

- Learn about JavaScript's history, role, and its usage on the web.
- Set up your development environment by installing Node.js and a code editor like Visual Studio Code.
- Write a simple "Hello, World!" program in JavaScript.


### Learn about JavaScript's history, role, and its usage on the web.
On commence par un gros copier coller Wikipédia. Sorry. Je vais juste mettre en gras les informations importantes.

JavaScript est un langage de programmation de scripts principalement employé dans les **pages web interactives** et à ce titre est une partie essentielle des applications web. Avec les langages HTML et CSS, JavaScript est au cœur des langages utilisés par les développeurs web. Une grande majorité des sites web l'utilisent, et **la majorité des navigateurs web disposent d'un moteur JavaScript pour l'interpréter**.

JavaScript est **aussi employé pour les serveurs Web** avec l'utilisation (par exemple) de Node.js ou de Deno.

JavaScript a été créé en 1995 par Brendan Eich et intégré au navigateur web Netscape Navigator 2.0. L'implémentation concurrente de JavaScript par Microsoft dans Internet Explorer jusqu'à sa version 9 se nommait JScript, tandis que celle d'Adobe Systems se nommait ActionScript. JavaScript a été **standardisé sous le nom d'ECMAScript** en juin 1997 par Ecma International dans le standard ECMA-262. La version en vigueur de ce standard depuis juin 2022 est la 13e édition.

C'est un **langage orienté objet à prototype** : les bases du langage et ses principales interfaces sont fournies par des objets. Cependant, à la différence d'un langage orienté objets, les objets de base ne sont pas des instances de classes. En outre, les fonctions sont des objets de première classe. Le langage **supporte le paradigme objet, impératif et fonctionnel**.
JavaScript est le langage possédant le plus large écosystème grâce à son **gestionnaire de dépendances npm**, avec environ 500 000 paquets en août 2017.

Revenons rapidement sur la notion de paradigme:
Lorsque l’on veut écrire un programme pour résoudre un problème, on choisit une manière d’écrire le code, une manière de structurer et d’écrire les instructions : on choisit un paradigme de programmation. C'est la manière de formuler la résolution du problème.

- **paradigme fonctionnel** : Le paradigme fonctionnel consiste à décomposer les programmes réalisés en un ensemble de fonctions.
  **En programmation fonctionnelle, l’ordre d’exécution du code n’a aucune importance**.
  Fonctions pures et impures :
  Les fonctions doivent idéalement produire des sorties qui ne dépendent strictement que de leurs arguments, sans que ces sorties ne dépendent de variables externes à la fonction elle-même. On parle alors de fonctions pures.
  A contrario, les fonctions qui ne respectent pas ce principe sont appelées des fonctions impures.
  Tout deviendra plus clair quand on parlera de scopes des fonctions plus tard.

  L’avantage principal du paradigme fonctionnel est de produire des codes courts et faciles à débugger. Il suffit de tester chacune de ses fonctions pour valider les codes.
  La programmation fonctionnelle n’est toutefois pas facile à appréhender, elle demande une certaine expertise. Elle ne convient de plus pas à toutes les tâches.

- **paradigme impératif**:  le plus ancien paradigme, il est à l’origine de nombreux langages de programmation tels que les langages C, Pascal ou Basic.
  Dans un paradigme impératif, les instructions sont exécutées de manière séquentielle, c’est-à-dire les unes après les autres dans l’ordre dans lequel elles ont été écrites. **En programmation impérative, l’ordre d’exécution du code a de l’importance**.
  Petite précision, on distingue deux sous-types de paradigmes impératifs :
  - le paradigme séquentiel
  - le paradigme procédural
  Leur différence tient dans le fait que la programmation procédurale autorise l’usage de fonctions pour réutiliser du code, alors que la programmation séquentielle ne l’autorise pas.

  L’avantage principal de la programmation impérative est que le code est très lisible, ce qui en facilite l’apprentissage.
  Ce paradigme produit toutefois vite des programmes volumineux, les codes peuvent ainsi perdre en clarté. De plus, en cas de modification ou de mise à jour du code, la programmation impérative peut induire un bon nombre de bugs puisque il faut relire le code dans son entier et effectuer de nombreuses retouches.


On aura l'occasion plus tard de pratiquer et de se rendre compte réellement des différences que les paradigmes impliquent.

Sources:
- https://fr.wikipedia.org/wiki/JavaScript
- https://www.maxicours.com/se/cours/utiliser-les-paradigmes-imperatifs-et-fonctionnels/

### Set up your development environment by installing Node.js and a code editor like Visual Studio Code.

Ce sera sans doute l'étape la plus facile et rapide de tout le programme !
J'utilise une machine virtuelle Ubuntu pour suivre ce programme, je vais donc utiliser apt pour installer Node. Adaptez en fonction de vos environnements :)

    sudo apt update
    sudo apt install nodejs
    node -v // nous retourne la version installée, juste pour vérifier que tout est ok
    sudo apt install npm // on aura aussi besoin de npm plus tard
    npm -v

Côté éditeur, chacun ses préférences et habitudes. Je commence le programme avec Atom qui est déjà installé sur cette VM mais je passerai peut-être sur VSC plus tard.

### Write a simple "Hello, World!" program in JavaScript.

On va écrire 2 types de Hello World différents, le premier, très simple, dans la console du navigateur et le second avec un serveur Node.js.

Console :
- ouvrir la console du navigateur (variable selon le navigateur mais souvent clic droit, inspecter ou F12 et choisir l'onglet Console en haut)
- taper "console.log('Hello World');" and voilà. La console du navigateur affiche notre message. Afficher des messages dans la console peut se révéler pratique pour débugger.

Node :
- RTFM (Read the f*cking manual) --> https://nodejs.org/en/docs/guides/getting-started-guide
Ici, pas grand chose de similaire à ce qu'on vient de faire juste avant. On ne va pas écrire un message dans la console mais on va faire tourner un serveur web qui, quand on le consultera nous retournera le texte "Hello World".
- On créé un fichier nommé app.js dans lequel on colle le code fourni par la doc
- On enregistre et on lance le serveur avec la commande "node app.js"
- En consultant l'url "http://localhost:3000" depuis un navigateur, on tombe sur notre page Hello World.
