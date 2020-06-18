## Lass die LEDs blinken

--- task ---

Verbinde deine LEDs mit folgenden Pins:

| LED  | GPIO-Stift |
| ---- |:----------:|
| Rot  |     22     |
| Gelb |     27     |
| Grün |     17     |

![PiStop verbunden mit GPIO 22, 27, 17 und Masse (ground)](images/Traffic-Lights-Diagram.png)

--- /task ---

--- task ---

Öffne **Mu** aus dem Hauptmenü. Klicke auf das **REPL** Symbol, um die Python-Shell zu öffnen.

--- /task ---

--- task ---

Gib die folgenden Befehle einzeln in die Python-Shell ein und beobachte die LED:

```python
from gpiozero import TrafficLights
Lichter = TrafficLights (22, 27, 17)
Lichter.on()
Lichter.off()
Lichter.blink()
```

--- /task ---

--- task ---

Versuche nun, die LED mit unterschiedlichen Geschwindigkeiten blinken zu lassen (die beiden Zahlen sind die **ein-Zeit** und die **aus-Zeit**):

```python
Lichter.blink(2, 2)
Lichter.blink(5, 5)
Lichter.blink(0.1, 0.1)
```

--- /task ---

--- task ---

Versuche nun, alle drei LEDs mit unterschiedlichen Geschwindigkeiten blinken zu lassen:

```python
Lichter.red.blink(1, 1)
Lichter.amber.blink(2, 2)
Lichter.green.blink(3, 3)

Red, amber und green sind Parameter des TrafficLight-Apis und stehen für die Farben rot, gelb und grün
```

--- /task ---