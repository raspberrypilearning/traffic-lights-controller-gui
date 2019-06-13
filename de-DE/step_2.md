## Lass die LEDs blinken

\--- task \---

Verbinde deine LEDs mit folgenden Pins:

| LED  | GPIO-Stift |
| ---- |:----------:|
| Rot  |     22     |
| Gelb |     27     |
| Grün |     17     |

![pi stop connected to gpio 22,27,17 and ground](images/Traffic-Lights-Diagram.png)

\--- /task \---

\--- task \---

Open **Mu** from the main menu. Click the **REPL** icon to open the Python shell.

\--- /task \---

\--- task \---

Gib die folgenden Befehle einzeln in die Python-Shell ein und beobachte die LED:

```python
from gpiozero import TrafficLights
lights = TrafficLights(22, 27, 17)
lights.on()
lights.off()
lights.blink()
```

\--- /task \---

\--- task \---

Versuche nun, die LED mit unterschiedlichen Geschwindigkeiten blinken zu lassen (die beiden Zahlen sind die **ein-Zeit** und die **aus-Zeit**):

```python
lights.blink(2, 2)
lights.blink(5, 5)
lights.blink(0.1, 0.1)
```

\--- /task \---

\--- task \---

Versuche nun, alle drei LEDs mit unterschiedlichen Geschwindigkeiten blinken zu lassen:

```python
lights.red.blink(1, 1)
lights.amber.blink(2, 2)
lights.green.blink(3, 3)
```

\--- /task \---