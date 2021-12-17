# React Native

Hey encore une chose de decouvert &#128513;

Parlons React mais pas just React mais native qui signifie que notre application tournera sur ios et android car React Native est cross-plateform.

J'ai decouvert React et je partage l'aventure avec vous &#129335;.

c'était un monde dans une planete &#127776; lointaine mais proche de Angular.

## Démarrer

---

Hi &#128075;!!!! Alors installons tout ce dont on a besoin pour commencer

### Installe NodeJs

```
sudo apt install nodejs
```

### Verifier l'installation

```
node --version
```

<img src="../../img/node-version.png"   />
### Installe Expo CLI

<p> J'ai decouvert ce framwork "expo" qui est magnifique, je vous mets le lien &#128073; <a href="https://docs.expo.dev/">EXPO</a> </p>
```
npm install --global expo-cli

```
### Créer un projet
```

expo init books

```

### Demarrer l'application
```

expo start

```

## Les composants capitaux
-------
Nous avons 7 composants principaux
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
### 1- Les Vues(View)
- Les **vues** ici sont appellées "user interface view sur Ios et android view sur android", sachez aussi que dans cette planette il faut décomposer son application en composants  &#9888;&#65039; tout en évitant d'avoir une panopluie de composant. Car, ceci est déconseillé.

**Style in line**
signifie que nous aurons deux accolades "{{}}" au niveau de style et on ne va pas l'écrire sur plusieurs lignes
La première signifie JavaScript et le second car c'est en inline
```

//Dans App.js
import React from "react";
import { Text, View } from "react-native";

const App = () => {
return <View style={{ borderWidth: 1, height: 150, width: 150 }}></View>;
};
export default App;

```
Bon écoutez je ne vais pas faire un cours, donc je vous donne encore un truc que je viens juste de capter.

<h5 style="color:green">Le mot clé Export</h5>

Le mots clé **"export"** pour utiliser un composant dans un autre il faut que dans le fichier où est defini le component l'exporter après sa definition, et l'importer dans le fichier où on l'utilise.

Ehh bhenn je viens de dire une chose truvial là &#128517 mais bon voici un exmple


<img src="../../img/component.gif"/>

### 2- Le composant Text
React n'accept pas les textes brutes donc il faut un composant texte pour la manipulation de texte
```

//Dans App.js
<Text style={{ color:"white", fontSize:20, fontWeight:"bold"}}>Bonjour Monsieur</Text>

```

### 3- Le composant StyleSheet
comme son nom l'indique il permet d'ecrire du css plus stylé &#128526;
```

//Dans App.js
import React from "react";
import { Text, View, StyleSheet } from "react-native";

const App = () => {
return (
<View style={styles.container}>
<Text style={styles.text}>Bonjour Monsieur</Text>
</View>
);
};
const styles = StyleSheet.create({
container: {
borderWidth: 1,
height: "100%",
width: "100%",
backgroundColor: "green",
justifyContent: "center",
alignItems: "center",
},
text: {
color: "white",
fontSize: 20,
fontWeight: "bold",
},
});
export default App;

```

<img src="../../img/stylesheet.png"/>
### 4- Le composant textInput
<div class="warning">Un composant sans enfant&#128551;? Ehh oui c'est quand on le ferme juste à la fin avec un "/" </div>
Au fur et à mesure qu'on ecrit dans un champs de saisie React fait la mise à jour donc pour eviter d'effacer ce que l'on écrit on utilise state.
```

//Dans App.js
import React, { useState } from "react";
import { Text, View, StyleSheet, TextInput } from "react-native";

const App = () => {
const [state, setState] = useState("");
return (
<View style={styles.container}>
<Text style={styles.text}>Bonjour Monsieur</Text>
<TextInput style={styles.input}
placeholder="Saisir du texte"
value={state}
onChangeText={(value)=>setState(value)}
/>
</View>
);
};
const styles = StyleSheet.create({
container: {
flex:1,
borderWidth: 1,
flexDirection:"column",
height: "100%",
width: "100%",
backgroundColor: "green",
justifyContent: "center",
alignItems: "center",
},
text: {
color: "white",
fontSize: 20,
fontWeight: "bold",
paddingBottom:20,
},
input:{
borderWidth:1,
height:30,
width:300,
fontSize:25,
color:"black"

}
});
export default App;

```
#### Props  et State
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

### 5- Le composant Image
##### Soit from assets:
importer d'abord l'image
```

import LOGO from "./assets/imgs.png";

```
puis on lui met du css
```

logo: {
width: 66,
height: 58,
margin: 10,
},

```
Enfin on met l'image dans une vue
```

<View style={styles.containerIm}>
  <Image style={styles.logo} source={LOGO} />
  
</View>
```
##### soit from une URL:
```
<View style={styles.containerIm}>
  <Image style={styles.logo} source={{uri: "https://reactnative.dev/img/tiny_logo.png"}} />
  
</View>
```
### 6- Le composant ScrollView
Il permet de faire defiler notre écran quand on aura beaucoup d'éléments à afficher.

### 7- Le composant FlatList
FlatList fait en sorte que lorsque nos informations sont sur le point d'apparaître, il supprime les éléments qui défilent hors de l'écran pour économiser de la mémoire et du temps de traitement.  

Egalement si vous voulez afficher des séparateurs entre vos éléments, plusieurs colonnes, un chargement de défilement infini ou tout autre nombre d'autres fonctionnalités qu'il prend en charge immédiatement. 
```

```
**Sources:**

<a href="https://openclassrooms.com/fr/courses/4902061-developpez-une-application-mobile-react-native/4915721-manipulez-le-state">openClassRooms</a>

<a href="https://reactnative.dev/docs/getting-started">React native doc</a>

