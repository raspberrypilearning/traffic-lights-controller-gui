## Laat de LED's knipperen

\--- task \---

Verbind je LED's met de volgende pinnen:

| LED         | GPIO-pin |
| ----------- |:--------:|
| Rood        |    22    |
| Oranje/geel |    27    |
| Groen       |    17    |

![pi stop verkeerslicht verbonden met gpio 22,27,17 en massa (ground)](images/Traffic-Lights-Diagram.png)

\--- /task \---

\--- task \---

Open **Mu** vanuit het hoofdmenu. Klik op het **REPL** pictogram om de Python shell te openen.

\--- /task \---

\--- task \---

Voer de volgende commando's één voor één in de Python-shell in en observeer de LED:

```python
from gpiozero import TrafficLights
lights = TrafficLights(22, 27, 17)
lights.on()
lights.off()
lights.blink()
```

\--- /task \---

\--- task \---

Probeer nu de LED's met verschillende snelheden te laten knipperen, de twee nummers zijn **on time** (tijd aan) en **off time**( tijd uit):

```python
lights.blink(2, 2)
lights.blink(5, 5)
lights.blink(0.1, 0.1)
```

\--- /task \---

\--- task \---

Probeer nu alle drie de LED's met verschillende snelheden te laten knipperen:

```python
lights.red.blink(1, 1)
lights.amber.blink(2, 2)
lights.green.blink(3, 3)
```

\--- /task \---