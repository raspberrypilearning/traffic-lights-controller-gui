## Erstellen Sie ein GUI

1. Öffne ein neues Fenster und speichere es. Jetzt schreibst du Code in diese Datei anstatt direkt in die Shell.

2. Erstelle eine GUI-Schaltfläche, um die rote LED einzuschalten:
    
    ```python
from guizero import App, Text, PushButton
from gpiozero import TrafficLights

lights = TrafficLights(22, 27, 17)

app = App()

PushButton(app, command=lights.red.on, text="on")

app.display()
```

![](images/guizero-1.png)

3. Füge eine Textbeschriftung und eine zweite Schaltfläche hinzu, um die rote LED auszuschalten:
    
    ```python
Text(app, "Red")
PushButton(app, command=lights.red.on, text="on")
PushButton(app, command=lights.red.off, text="off")
```

![](images/guizero-2.png)

4. Gib deiner App einen Namen und verwende das Rasterlayout:
    
    ```python
app = App("Traffic Lights controller", layout="grid")

Text(app, "Red", grid=[0, 0])
PushButton(app, command=red.on, text="on", grid=[0, 1])
PushButton(app, command=red.off, text="off", grid=[0, 2])
```

![](images/guizero-3.png)