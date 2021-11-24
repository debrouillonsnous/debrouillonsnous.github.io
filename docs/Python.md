# Python 

## Démarrer avec python
Un autre language Python!!
C'est un langage de programmation multiplateforme que nous pouvons donc exécuter sur plusieurs plates-formes telles que Windows, macOS, Linux et a même été porté sur les machines virtuelles. Il est totalement gratuit et open source.

**Ohh mince j'ai Lunix!**  
Si vous avez Lunix ou Mac vous verrez qu'il est déjà installé sauf que la plupart des versions installées sont obsolètes donc c'est à vous d'installer la nouvelle version ou la version de travaille qu'il vous faut.

**`Dans ce tutoriel nous travaillerons exclusivement sur Ubuntu `**
### Installation
Je vous mets le lien de la documentation pour le téléchargement ou l'obtention du package.

Téléchargez la [ dernière version](https://www.python.org/) de Python.  
Plus specifiquement pour Ubuntu:

Mis à jour des paquages et installé les prérequis:
```
sudo apt update
sudo apt install software-properties-common
```
Ajoutez le PPA deadsnakes à la liste des sources de votre système ([c'est quoi un PPA?](https://doc.ubuntu-fr.org/ppa)):
```
sudo add-apt-repository ppa:deadsnakes/ppa
```
Maintenant installons python 3.9: 
```
sudo apt install python3.9
```
Vérifions si python s'est bien installé:
```
python3.9 --version
```
## Mon premier programme
En haut nous avons installé python3.9, maintenant écrivons notre premier programme en python.
![script](../../img/hello_world.gif?raw=true "Title")

## The Basics
### Les Variables
Une variable est une place où on peut stoker des variables
Vous pouvez stoker tout ce que vous voulez
```
Nom = "Barry"
print(Nom)
age = 3
taille = 2.01
liste_nombre = [1,2,3,4]

Nom , age, taille = "Barry", 3, 2.01
```
<img src="../../img/variables.gif" alt="drawing" style="width:50%; height:300px"/>
## Operators
## List comprehension
## github copilot
## sublime merge
## Control Flow
## Loops
## Functions
## Classes
### Design pattern
## Working with Dates
## Working with Files
## Fetching Data from Internet
## Modules
## Décorateurs

