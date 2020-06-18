## Fais clignoter les LED

\--- task \---

Connecte les LEDs aux broches suivantes :

| LED    | GPIO pin |
| ------ |:--------:|
| Rouge  |    22    |
| Orange |    27    |
| Verte  |    17    |

![pi stop connecté aux gpio 22, 27, 17 et masse](images/Traffic-Lights-Diagram.png)

\--- /task \---

\--- task \---

Ouvre **Mu** depuis le menu principal. Cliquez sur l'icône **REPL** pour ouvrir le shell Python.

\--- /task \---

\--- task \---

Entre les commandes suivantes, une par une, dans le shell Python et observe les LEDs :

```python
from gpiozero import TrafficLights
lampes = TrafficLights(22, 27, 17)
lampes.on()
lampes.off()
lampes.blink()
```

\--- /task \---

\--- task \---

Essaie maintenant de faire clignoter les LEDs à différentes vitesses (les deux chiffres sont ** temps allumé ** et ** temps éteint ** ) :

```python
lampes.blink(2, 2)
lampes.blink(5, 5)
lampes.blink(0.1, 0.1)
```

\--- /task \---

\--- task \---

Maintenant, essaie de faire clignoter les trois LEDs à des rythmes différents :

```python
lampes.red.blink(1, 1)
lampes.amber.blink(2, 2)
lampes.green.blink(3, 3)
```

\--- /task \---