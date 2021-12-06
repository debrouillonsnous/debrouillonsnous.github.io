# React Native
Hey encore une chose de decouvert &#128513;

Parlons React mais pas just React mais native qui signifie que notre application tournera sur ios et android car React Native est cross-plateform.

J'ai decouvert React et je partage l'aventure avec vous &#129335;.

c'était un monde dans une planete &#127776; lointaine mais proche de Angular.

<p> J'ai decouvert ce framwork "expo" qui est magnifique, je vous mets le lien &#128073; <a href="https://docs.expo.dev/">EXPO</a> </p>
## Views et Components
- Les **vues** ici sont appellées "user interface view sur Ios et android view sur android", sachez aussi que dans cette planette il faut décomposer son application en composants  &#9888;&#65039; tout en évitant d'avoir une panopluie de composant. Car, ceci est déconseillé.

- un **composant** est une classe(transmettre des props) ou une fonction(mais elle renvoie rarement des props).

La manière la plus simple de definir un component est de créer une fonction JavaScript.

Nous appelons ces composants "composants de fonction" car il s'agit littéralement de fonctions JavaScript.
```
import React from 'react';
import { Text, View } from 'react-native';

const HelloWorldApp = () => {
  return (
    <View style={{
        flex: 1,
        justifyContent: 'center',
        alignItems: 'center'
      }}>
      <Text>Hello, world!</Text>
    </View>
  );
}

export default HelloWorldApp;
```
Les deux composants ci-dessus sont équivalents du point de vue de React.
```
import React, { Component } from 'react';
import { Text, View } from 'react-native';

class HelloWorldApp extends Component {
  render() {
    return (
      <View style={{
          flex: 1,
          justifyContent: "center",
          alignItems: "center"
        }}>
        <Text>Hello, world!</Text>
      </View>
    );
  }
}

export default HelloWorldApp;
```

Bon écoutez je ne vais pas faire un cours, donc je vous donne encore un truc que je viens juste de capter.
## Export
Le mots clé **"export"** pour utiliser un composant dans un autre il faut que dans le fichier où est defini le component l'exporter après sa definition, et l'importer dans le fichier où on l'utilise. 

Ehh bhenn je viens de dire une chose truvial là &#128517 mais bon voici un exmple


<img src="../../img/component.gif"/>

## Props  et State
Parlons des state et de props:
Les props nous permettent de contrôler un component, 
En langage plus technique, ils sont accessibles en lecture uniquement par le component fils.


<div class="warning">
Attention,ne pensez pas que les props d'un component ne peuvent pas changer. <br>Elles le peuvent ; simplement, c'est le component parent qui va les changer.
</div>
C'est là qu'intervient **"state"** il nous permet de récuperer les nouvelles données avec setState et indiquer à React que le component a besoin d'être re-rendu avec ces  nouvelles données.

```
  const [tasks, setTask] = useState([
    { title: "Nouvelle tache", completed: false },
  ]);
```
<div class="info">Le state et les props gèrent les données de vos components.</div>

## Les formulaire
### TextInput

**Sources:**

<a href="https://openclassrooms.com/fr/courses/4902061-developpez-une-application-mobile-react-native/4915721-manipulez-le-state">openClassRooms</a>

<a href="https://reactnative.dev/docs/getting-started">React native doc</a>