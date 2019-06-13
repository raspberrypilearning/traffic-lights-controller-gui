## Erstelle ein GUI

\--- task \---

Close the REPL. Now you'll write code into a file rather than directly in the shell.

\--- /task \---

\--- task \---

Erstelle eine GUI-Schaltfläche, um die rote LED einzuschalten:

```python
from guizero import App, Text, PushButton
from gpiozero import TrafficLights

lampen = TrafficLights(22, 27, 17)

app = App()

PushButton(app, command=lampen.red.on, text="ein")

app.display()
```

![](images/guizero-1.png)

\--- /task \---

\--- task \---

Füge eine Textbeschriftung und eine zweite Schaltfläche hinzu, um die rote LED auszuschalten:

```python
Text(app, "Rot")
PushButton(app, command=lampen.red.on, text="ein")
PushButton(app, command=lampen.red.off, text="aus")
```

![](images/guizero-2.png)

\--- /task \---

\--- task \---

Gib deiner App jetzt einen Namen und verwende das Rasterlayout:

```python
app = App("Traffic Lights controller", layout="grid")

Text(app, "Red", grid=[0, 0])
PushButton(app, command=lights.red.on, text="on", grid=[1, 0])
PushButton(app, command=lights.red.off, text="off", grid=[2, 0])
```

![](images/guizero-3.png)

\--- /task \---