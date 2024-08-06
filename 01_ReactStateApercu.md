# Chapitre : REACT STATE - APERCU


# Introduction

Lors du développement d'applications avec React, vous disposez de deux manières de conserver les données :

1. Les accessoires React que nous avons rencontrés précédemment.
2. L'état du composant que nous verrons dans cette super compétence.

Dans cette super compétence, nous allons apprendre :

* Qu'est-ce que l'État ?
* Comment utiliser l'état dans React ?
* Qu’est-ce que le cycle de vie d’un composant ?

# Qu'est-ce qu'un État ?

State est un objet Javascript qui stocke les données dynamiques d'un composant et détermine le comportement des composants. Comme State est dynamique, il permet à un composant de suivre l'évolution des informations, tout en les rendant, afin qu'il soit plus dynamique et interactif.

# Pourquoi utiliser l'état ?

En fait, le DOM virtuel de React ne permet aucune modification aléatoire des données. Nous devons initialiser puis modifier les données dans State, c'est donc comme si nous décrivions le scénario pour React, puis l'application se chargera de toutes les modifications.

Avant la version 16.8, React utilisait le composant basé sur les classes pour gérer le composant avec état. Après cette mise à jour majeure, l'équipe principale de React nous a donné la possibilité de gérer l'état même dans un composant fonctionnel à l'aide des hooks React.

# Comment utiliser l'État ?

Commençons par examiner l'état avant la version 16.8. Comme nous l'avons dit précédemment, l'état n'était utilisé que dans un composant basé sur une classe. Ainsi, pour définir un état dans une classe, vous pouvez simplement suivre l'exemple ci-dessous :

```
import React from "react";
class Welcome extends React.Component {
 state = {
   name: "Sara"
 };
 render() {
   return <h1>hello {this.state.name}</h1>;
 }
}
export default Welcome;
```

Un état est un objet Javascript qui peut contenir n'importe quel type de données.

# Comment utiliser l'État ?

Un état doit être aussi simple que possible. Il ne peut être défini qu'à l'aide de la méthode **setState()** et l'appel de cette méthode déclenche les mises à jour de l'interface utilisateur.
L'état représente l'état local du composant. Il n'est accessible ou modifiable qu'à l'intérieur du composant.

```
class Welcome extends React.Component {
 state = {
   name: "Sara"
 };
 handleClick=()=>this.setState({name:'Arya'})
 render() {
   return(
     <>
     <h1>Hello {this.state.name}</h1>
     <button onClick={this.handleClick}> ClickMe</button>
     </>
   )
 }
}
```

Doc utiles :

    -	https://www.simplilearn.com/what-is-reactjs-state-article

    -	https://codesandbox.io/s/classmanagingstate-i7leo
