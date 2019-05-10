## Create a GUI

\--- task \---

Close the REPL. Now you'll write code into a file rather than directly in the shell.

\--- /task \---

\--- task \---

Create a GUI button to turn the red LED on:

```python
from guizero import App, Text, PushButton
from gpiozero import TrafficLights

lights = TrafficLights(22, 27, 17)

app = App()

PushButton(app, command=lights.red.on, text="on")

app.display()
```

![](images/guizero-1.png)

\--- /task \---

\--- task \---

Add a text label and a second button to turn the red LED off:

```python
Text(app, "Red")
PushButton(app, command=lights.red.on, text="on")
PushButton(app, command=lights.red.off, text="off")
```

![](images/guizero-2.png)

\--- /task \---

\--- task \---

Now give your app a name, and use the grid layout:

```python
app = App("Traffic Lights controller", layout="grid")

Text(app, "Red", grid=[0, 0])
PushButton(app, command=lights.red.on, text="on", grid=[1, 0])
PushButton(app, command=lights.red.off, text="off", grid=[2, 0])
```

![](images/guizero-3.png)

\--- /task \---