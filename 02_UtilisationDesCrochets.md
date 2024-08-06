# Chapitre : UTILISATION DES CROCHETS


# Utilisation des crochets

Après la version 16 (utilisant des Hooks), dans notre cas, nous utiliserons des Hooks pour pouvoir contrôler notre état à l'intérieur du composant. Passons donc en revue ces Hooks.

Les hooks ont été récemment introduits dans React en février 2019 et constituent une fonctionnalité révolutionnaire. Ce concept tend à changer la façon dont nous écrivons du code dans un certain composant de notre application.

Les hooks ont été considérés comme une solution potentielle aux problèmes des applications React grâce à leur simplicité et à leurs nouvelles fonctionnalités.
Désormais, nous pouvons accéder à l'état même dans le composant fonctionnel.

***PS** . Nous étudierons les hooks React en détail dans les prochaines compétences. Nous venons d'utiliser useState dans cette compétence.*

## Commençons:

Nous utiliserons ce composant pour introduire les Hooks car nous l'analyserons plus en détail :

```
const MyFunctionComponent = () => {
 // setting the state hooks
 const [name, setName] = useState("Arya Stark");
 return (
   <div>
     <p>hello my name is {name}</p>
   </div>
 );
};
```

Pour expliquer le code, nous avons d'abord déclaré une variable d'état puis nous avons stocké un nom avec la valeur "Arya Stark" et enfin, nous avons accédé à notre composant pour afficher le nom.

Presentation des crochets

    -	https://legacy.reactjs.org/docs/hooks-intro.html

Crochet useState

    -	https://legacy.reactjs.org/docs/hooks-state.html
