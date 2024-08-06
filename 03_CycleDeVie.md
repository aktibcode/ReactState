# Chapitre : CYCLE DE VIE


# Cycle de vie

Chaque composant React possède son propre cycle de vie. Le
cycle de vie d'un composant peut être défini comme la série de méthodes qui sont invoquées à différentes étapes de l'existence du composant.

Un composant React peut passer par trois étapes de vie.
Chaque composant de React possède un cycle de vie que nous pouvons surveiller et manipuler au cours de ses trois phases principales.

Les trois phases sont :

1. **Montage** : La première phase du cycle de vie du composant est celle où les éléments sont placés dans le DOM.
2. **Mise à jour** : La deuxième phase du cycle de vie est celle où un composant est mis à jour.
3. **Démontage** : La phase finale du cycle de vie est celle où un composant est supprimé du DOM.

# Montage

Cette phase est la première phase du cycle de vie du composant. Elle contient quatre méthodes qui sont invoquées dans cet ordre, lorsqu'une instance d'un composant est créée et insérée dans le DOM :

1. `Constructor()`: Cette méthode est appelée lorsque le composant est initialisé. La méthode constructeur est l'endroit où nous déclarons l'état et passons les props comme arguments.
2. `getDerivedStateFromProps()`: Cette méthode est appelée avant le rendu des éléments dans le DOM. getDerivedStateFromProps n'existe que dans un seul but. Elle permet à un composant de mettre à jour son état interne en fonction des modifications apportées aux propriétés.
3. `render()`: Cette méthode est la seule méthode requise lorsque l'on travaille avec des classes. Elle examine les props et les états et renvoie l'élément à restituer.
4. `ComponentDidMount()`:Cette méthode est invoquée immédiatement après le rendu du composant et c'est l'endroit idéal pour appeler la méthode setState.

# Mise à jour

Lorsque l'état ou les propriétés sont mis à jour, le composant entre dans cette phase de son cycle de vie. Cette phase contient cinq méthodes invoquées dans cet ordre :

1. `getDerivedStateFromProps()`: Cette méthode est la même que celle de la phase de montage. Elle renvoie un objet pour mettre à jour l'état ou renvoie null s'il n'y a pas de mise à jour.
2. `shouldComponentUpdate()`: Cette méthode est la deuxième méthode à invoquer dans cette phase. Elle définira soit le composant qui sera mis à jour, soit non, selon que les props ou l'état sont modifiés ou non.
3. `render()`:Le même que celui de la phase de montage, sauf qu'il sera restitué en fonction des nouveaux accessoires/état.
4. `getSnapshotBeforeUpdate()`: Cette méthode est invoquée juste avant que l'élément le plus récemment rendu ne soit validé. Elle nous donne la possibilité de capturer certaines informations du DOM, avant qu'elles ne changent potentiellement.
5. `componentDidUpdate()`: cette méthode est appelée immédiatement après la mise à jour.

# Démontage

Le composant entre dans cette phase à la fin de sa vie, ce qui signifie qu'il sera supprimé du DOM.

1. `componentWillUnmount()`: Cette méthode est appelée immédiatement avant la fin du cycle de vie du composant. C'est l'endroit idéal pour nettoyer notre composant.

## Résumer:

<iframe allowfullscreen="true" frameborder="0" src="https://www.youtube.com/embed/Dxo3X16N75U?list=PL-w_yrNy8uTaWNAYCFoyW0C0zPm4S9b3v"></iframe>

# Résumons!

Pour résumer ce que nous avons vu, le composant passe par trois phases principales au cours de son cycle de vie. Chaque phase contient des méthodes à invoquer dans un certain ordre. Dans certains cas, nous devons modifier le comportement de ces méthodes afin d'accomplir des tâches spécifiques.
Dans l'image ci-dessous, il y a une description visuelle de ces phases.

![](https://miro.medium.com/max/1400/1*cPwvUhZrnB1dtZnjBEfXfA.png)



Ces ressources peuvent vous aider

Cycle de vie de la classe

[https://reactjs.org/docs/state-and-lifecycle.html#adding-lifecycle-methods-to-a-class](https://reactjs.org/docs/state-and-lifecycle.html#adding-lifecycle-methods-to-a-class)

Crochet de cycle de vie

[https://reactjs.org/docs/hooks-effect.html](https://reactjs.org/docs/hooks-effect.html)
