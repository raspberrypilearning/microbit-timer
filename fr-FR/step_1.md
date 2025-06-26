Il peut arriver que tu aies besoin de temps pour quelque chose.

Tu peux afficher un minuteur sur les LED de la manière suivante.

```microbit
input.onGesture(Gesture.Shake, function () {
    for (let second = 0; second <= 4; second++) {
        basic.showNumber(second + 1)
        basic.pause(1000)
    }
    basic.showIcon(IconNames.EighthNote)
    basic.clearScreen()
})
```

Dans ce code :

La variable `seconde`{:class='microbitvariables'} prend sur chaque valeur de `0` au nombre final (`4` dans notre exemple) et compte un par un.

La valeur de la variable `seconde`{:class='microbitvariables'} est ajoutée à `1` et le total est affiché sur les LED pendant une seconde (la durée définie dans le bloc `pause`{:class='microbitbasic'}).

Après le dernier nombre (`5`) affiché, le bloc `montrer l'icône`{:class='microbitbasic'} est utilisé pour afficher une note musicale, puis les LED sont désactivées en utilisant le bloc `effacer l'écran`{:class='microbitbasic'}.

L'exemple montre que le minuteur démarre lorsque le micro:bit est secoué, mais tu peux le régler pour qu'il démarre lors d'autres événements ; par exemple, lorsqu'un bouton est pressé. Tu peux également le placer dans une fonction si tu souhaites l'appeler à différents endroits de ton code.

### Modifier la durée du minuteur

Tu peux modifier la durée du minuteur en modifiant le deuxième nombre dans le bloc `pour`{:class='microbitloops'}. Définis-le sur un nombre inférieur au nombre sur lequel tu veux terminer (n'oublie pas que le bloc `+`{:class='microbitmath'} est utilisé).

### On compte à l’envers, pas à l’endroit

Pour créer un compte à rebours, tu dois soustraire la valeur de la variable `seconde`{:class='microbitvariables'} du nombre final (`4` dans cet exemple) plus un (donc `5` dans cet exemple).

Voici comment tu modifieras le code.

```microbit
input.onGesture(Gesture.Shake, function () {
    for (let second = 0; second <= 4; second++) {
        basic.showNumber(5 - second)
        basic.pause(1000)
    }
    basic.showIcon(IconNames.EighthNote)
    basic.clearScreen()
})
```
