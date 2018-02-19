## Lass die LEDs blinken

1. Öffne Python 3 aus dem Hauptmenü.

2. Gib die folgenden Befehle einzeln in die Python-Shell ein und beobachte die LED:
    
    (Bitte die Größer-Zeichen nicht eingeben `>>>`)
    
    ```python
>>> from gpiozero import TrafficLights
>>> lampen = TrafficLights(22, 27, 17)
>>> lampen.on()
>>> lampen.off()
>>> lampen.blink()
```

3. Versuche nun, die LED mit unterschiedlichen Geschwindigkeiten blinken zu lassen (die beiden Zahlen sind die **ein-Zeit** und die **aus-Zeit**):
    
    ```python
>>> lampen.blink(2, 2)
>>> lampen.blink(5, 5)
>>> lampen.blink(0.1, 0.1)
```

4. Versuche nun, alle drei LEDs mit unterschiedlichen Geschwindigkeiten blinken zu lassen:
    
    ```python
>>> lampen.red.blink(1, 1)
>>> lampen.amber.blink(2, 2)
>>> lampen.green.blink(3, 3)

Red, amber und green sind Parameter des TrafficLight-APIs und stehen für die Farben rot, gelb und grün.
```