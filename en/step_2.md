## Flash the LEDs

--- task ---

Connect your LEDs to the following pins:

| LED   | GPIO pin |
| ----- | :------: |
| Red   |    22    |
| Amber |    27    |
| Green |    17    |

![pi stop connected to gpio 22,27,17 and ground](images/Traffic-Lights-Diagram.png)

--- /task ---

--- task ---

Open **Mu** from the main menu. Click the **REPL** icon to open the Python shell.

--- /task ---

--- task ---

Enter the following commands, one-by-one, into the Python shell, and observe the LED:

```python
from gpiozero import TrafficLights
lights = TrafficLights(22, 27, 17)
lights.on()
lights.off()
lights.blink()
```

--- /task ---

--- task ---

Now try blinking the LED at different speeds (the two numbers are **on time** and **off time**):

```python
lights.blink(2, 2)
lights.blink(5, 5)
lights.blink(0.1, 0.1)
```

--- /task ---

--- task ---

Now try flashing all three LEDs at different rates:

```python
lights.red.blink(1, 1)
lights.amber.blink(2, 2)
lights.green.blink(3, 3)
```

--- /task ---
