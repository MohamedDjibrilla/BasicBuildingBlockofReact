Bonjour,
Bienvenue dans ce didacticiel, aujourd'hui je vais vous apprendre à démarrer avec React et React Native.

Qu'est-ce que React?
En termes simples, React est «une bibliothèque JavaScript pour créer des interfaces utilisateur». Pensez à React comme:
Déclaratif
React facilite la création d'interfaces utilisateur interactives. Concevez des vues simples pour chaque état de votre application, et React mettra à jour et restituera efficacement les bons composants lorsque vos données changent.

Basé sur les composants
Créez des composants encapsulés qui gèrent leur propre état, puis composez-les pour créer des interfaces utilisateur complexes. Étant donné que la logique des composants est écrite en JavaScript au lieu de modèles, vous pouvez facilement transmettre des données riches via votre application et garder l'état hors du DOM.

Apprenez une fois, écrivez n'importe où
Nous ne faisons pas d'hypothèses sur le reste de votre pile technologique, vous pouvez donc développer de nouvelles fonctionnalités dans React sans réécrire le code existant.
React peut également effectuer le rendu sur le serveur à l'aide de Node et alimenter les applications mobiles à l'aide de React Native.


React Vs React Native:

Bien qu'il existe plusieurs similitudes entre Reactjs et React Native, il existe également des différences notables. Regardons:
• Reactjs peut être décrit comme un dérivé de base de React DOM, pour la plate-forme Web, tandis que React Native est un dérivé de base en soi, ce qui signifie que la syntaxe et le flux de travail restent les mêmes, mais que les composants changent.
• Reactjs, finalement, est une bibliothèque JavaScript, qui permet au programmeur de créer une couche d'interface utilisateur attrayante et très performante, tandis que React Native est un framework complet pour créer des applications multiplateformes, que ce soit Web, iOS ou Android.
• Dans Reactjs, le DOM virtuel est utilisé pour rendre le code du navigateur dans Reactjs tandis que dans React Native, les API natives sont utilisées pour rendre les composants dans mobile.
• Les applications développées avec Reactjs rendent le HTML dans l'interface utilisateur tandis que React Native utilise JSX pour le rendu de l'interface utilisateur, qui n'est rien d'autre que du javascript.
• CSS est utilisé pour créer un style dans Reactjs tandis qu'une feuille de style est utilisée pour créer un style dans React Native.
• Dans Reactjs, l'animation est possible, en utilisant CSS, tout comme le développement Web tandis que dans React Native, une API animée est utilisée pour induire une animation à travers différents composants de l'application React Native.
• Si le besoin est de créer une interface utilisateur hautement performante, dynamique et réactive pour les interfaces Web, Reactjs est la meilleure option tandis que si le besoin est de donner aux applications mobiles un sentiment vraiment natif, React Native est la meilleure option.
Plus d'informations peuvent être lues sur (https://www.simform.com/reactjs-vs-reactnative/#:~:text=In%20Reactjs%2C%20virtual%20DOM%20is,which%20is%20nothing%20but%20javascript. )

Comment mettre en place?
Conditions préalables:To be able to work through this guide, you need:
• Système d'exploitation Windows
• 4 Go d'espace mémoire ROM.
React peut être exécuté et débogué sur des périphériques virtuels et physiques. Pour les besoins de ce tutoriel, nous allons utiliser l'application expo disponible dans le Google Play Store. Alors commençons, profitez de votre tutoriel.

Configuration de votre environnement
L'écosystème React Native a beaucoup évolué depuis la première édition. L'outil open source Expo.io, en particulier, a rationalisé à la fois les phases d'initialisation et de développement du projet, rendant le travail dans React Native encore plus agréable qu'il ne l'était déjà dans la version 0.36.
Avec le flux de travail de l'Expo, vous pourrez créer des applications iOS et Android natives en utilisant uniquement JavaScript, travailler dans le simulateur iOS et l'émulateur Android avec rechargement en direct et tester sans effort votre application sur n'importe quel appareil du monde réel via l'application d'Expo. Jusqu'à ce que vous ayez besoin d'accéder au code natif (par exemple, pour l'intégrer au code natif hérité à partir d'une base de code séparée), vous pouvez développer votre application entièrement en JavaScript sans jamais avoir besoin d'utiliser Xcode ou Android Studio. Si votre projet doit évoluer vers la prise en charge du code natif, Expo offre la possibilité de détacher votre projet, ce qui transforme votre application en code natif pour une utilisation dans Xcode et Android Studio.
Installation de Node.JS
Node.js est un moteur d'exécution JavaScript basé sur le moteur JavaScript V8 de Chrome et conçu pour créer des applications réseau évolutives. Node permet d'exécuter JavaScript dans un terminal et constitue un outil indispensable pour tout développeur Web. Pour plus d'informations sur ce qu'est Node.js, vous pouvez lire la page About Node.js du projet sur https://nodejs.org/en/about/. Téléchargez et installez Node.js à partir du site du projet à l'adresse https://nodejs.org/en/download/.

La partie la plus difficile de la configuration est terminée! À partir de maintenant, nous pouvons utiliser la magie fournie par Expo pour créer facilement de nouvelles applications pour le développement. Nous allons créer notre première application en utilisant Expo via la ligne de commande (CMD) en suivant les étapes suivantes:Get the command line tool
You will run this tool locally to package, serve, and publish your projects.

npm install expo-cli --global

Create your first project
Il vous sera demandé de créer un compte Expo avant de continuer.
expo init myNewProject
cd myNewProject
expo start

Prévisualisez votre projet
Ouvrez le client de développement Expo sur votre appareil. Scannez le code QR imprimé par expo start avec Expo Client (Android) ou Appareil photo (iOS). Vous devrez peut-être attendre une minute pendant que votre projet se regroupe et se charge pour la première fois.

Pour une liste de toutes les commandes disponibles pour l'Expo CLI, consultez la documentation à l'adresse https://docs.expo.io/versions/latest/guides/expo-cli.html.

Structure native de réaction et de réaction de base
my-app
├── build
├── node_modules
├── public
│   ├── favicon.ico
│   ├── index.html
│   └── manifest.json
├── src
│   ├── App.css
│   ├── App.js
│   ├── App.test.js
│   ├── index.css
│   ├── index.js
│   ├── logo.svg
│   └── serviceWorker.js
├── .gitignore
├── package.json
└── README.md
•	build est l'emplacement de votre version finale prête pour la production. Ce répertoire n'existera pas tant que vous n'exécuterez pas npm build ou yarn build. Le contenu de ce dossier doit être prêt à être expédié sans aucune interaction de votre part.node_modules is where packages installed by NPM or Yarn will reside.
•	• public est l'endroit où résident vos fichiers statiques. Si le fichier n'est pas importé par votre application JavaScript et doit conserver son nom de fichier, placez-le ici. Les fichiers du répertoire public conserveront le même nom de fichier en production, ce qui signifie généralement qu'ils seront mis en cache par votre client et ne seront plus jamais téléchargés. Si votre fichier n'a pas de nom de fichier important, tel que index.html, manifest.json ou robots.txt, vous devez le mettre dans src à la place.
•	src est l'endroit où résident vos fichiers dynamiques. Si le fichier est importé par votre application JavaScript ou change de contenu, placez-le ici. Afin de s'assurer que le client télécharge la version la plus à jour de votre fichier au lieu de s'appuyer sur une copie en cache, Webpack attribuera aux fichiers modifiés un nom de fichier unique dans la version de production. Cela vous permet d'utiliser des noms de fichiers simples et intuitifs pendant le développement, tels que banner.png au lieu de banner-2019-03-01-final.png. Vous n'avez jamais à vous soucier du fait que votre client utilise la copie mise en cache obsolète, car Webpack renomme automatiquement banner.png en banner.unique-hash.png, où le hachage unique ne change que lorsque banner.png change.

Blocs de construction de base:
Components:
Les programmes natifs React et React sont constitués d'interfaces utilisateur interconnectées les unes aux autres.
Ces interfaces utilisateur sont appelées composants. Nous avons deux types de composants:
Composant fonctionnel:
La manière la plus simple de définir un composant est d'écrire une fonction JavaScript::

function HelloWorld (props) {
  return <h1>Hello World</h1>;
}
Cette fonction est un composant React valide car elle accepte un seul argument d'objet «props» (qui signifie propriétés) avec des données et renvoie un élément React. Nous appelons ces composants «composants de fonction» car ce sont littéralement des fonctions JavaScript.

Le class component:
Vous pouvez également utiliser une classe ES6 pour définir un composant:
class HelloWorld extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
      </div>
    );
  }
}
On peut convertir un composant de fonction comme HelloWorld en une classe en quatre étapes:
• Créez une classe ES6, avec le même nom, qui étend React.Component.
• Ajoutez-lui une seule méthode vide appelée render ().
• Déplacez le corps de la fonction dans la méthode render ().
• Supprimer la déclaration de fonction vide restante

En fonction de la librairie (react / react native) utilisée, on peut avoir de nombreux types de composants:
Pour les composants de réaction, vous pouvez en lire plus sur https://reactjs.org/docs/react-component.html#gatsby-focus-wrapper.
Pour les composants natifs de réaction, vous pouvez en lire plus sur https://reactnative.dev/docs/components-and-apis.







Props (propriétés)
Props est l'abréviation de «propriétés». Les propriétés vous permettent de personnaliser les composants React. Par exemple, ici, vous passez à chaque <Cat> un nom différent pour le rendu de Cat:
import React from 'react';
import { Text, View } from 'react-native';
const Cat = (props) => {
  return (
    <View>
      <Text>Hello, I am {props.name}!</Text>
    </View>
  );
}
const Cafe = () => {
  return (
    <View>
      <Cat name="John" />
      <Cat name="Lory" />
      <Cat name="Lore" />
    </View>
  );
}
export default Cafe;

 
La plupart des composants principaux de React et React Native peuvent également être personnalisés avec des accessoires.

Etat :
Bien que vous puissiez considérer les propriétés comme des arguments que vous utilisez pour configurer le rendu des composants, l'état est comme le stockage des données personnelles d'un composant. L'état est useful for handling data that changes over time or that comes from user interaction. State gives your components memory!
import React, { useState } from "react";
import { Button, Text, View } from "react-native";

const Cat = (props) => {
  const [isHungry, setIsHungry] = useState(true);

  return (
    <View>
      <Text>
        Je m'appelle {props.name}, et {isHungry ? "J'ai faim" : "Je suis plein"}!
      </Text>
      <Button
        onPress={() => {
          setIsHungry(false);
        }}
        disabled={!isHungry}
        title={isHungry ? "Donnez moi a manger" : "Merci!"}
      />
    </View>
  );
}

const Cafe = () => {
  return (
    <>
      <Cat name="John" />
      <Cat name="Jane" />
    </>
  );
}

export default Cafe;
 

Tout d'abord, vous voudrez importer useState depuis React comme ceci: 
import React, { useState } from 'react';
Ensuite, vous déclarez l'état du composant en appelant useState dans sa fonction. Dans cet exemple, useState crée une variable d'état isHungry:
const Cat = (props) => {
  const [isHungry, setIsHungry] = useState(true);
  // ...
};
Vous pouvez utiliser useState pour suivre tout type de données: chaînes, nombres, booléens, tableaux, objets. Par exemple, vous pouvez suivre le nombre de fois qu'un chat a été caressé avec const [timesPetted, setTimesPetted] = useState (0)!
L'appel de useState fait deux choses:
• il crée une «variable d'état» avec une valeur initiale - dans ce cas, la variable d'état est isHungry et sa valeur initiale est true
• il crée une fonction pour définir la valeur de cette variable d’état - setIsHungry
Peu importe les noms que vous utilisez. Mais il peut être pratique de considérer le modèle comme [<getter>, <setter>] = useState (<initialValue>).
Ensuite, vous ajoutez le composant Button Core et lui donnez une propriété onPress:
<Button  onPress={() => {
    setIsHungry(false);
  }}
  //..
/>
Maintenant, quand quelqu'un appuie sur le bouton, onPress se déclenche, appelant le setIsHungry (false). Cela définit la variable d'état isHungry sur false. Lorsque isHungry a la valeur false, la prop désactivée du Button est définie sur true et son titre change également:
<Button
  //..
  disabled={!isHungry}
  title={isHungry ? 'Donnez moi a manger' : 'Merci!'}
/>
Vous avez peut-être remarqué que même si isHungry est un const, il est apparemment réaffectable! Ce qui se passe, c'est lorsqu'une fonction de définition d'état comme setIsHungry est appelée, son composant sera rendu à nouveau. Dans ce cas, la fonction Cat s'exécutera à nouveau - et cette fois, useState nous donnera la valeur suivante de isHungry.
Enfin, placez vos chats dans un composant Cafe:
const Cafe = () => {
  return (
    <>
      <Cat name="John" />
      <Cat name="Jane" />
    </>
  );
};






#
