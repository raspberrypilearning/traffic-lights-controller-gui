## Lass die LEDs blinken

1. Öffne Python 3 aus dem Hauptmenü.

2. Gib die folgenden Befehle einzeln in die Python-Shell ein und beobachte die LED:
    
    (Bitte die Größer-Zeichen nicht eingeben `>>>`)
    
    ```python
>>> from gpiozero import TrafficLights
>>> lights = TrafficLights(22, 27, 17)
>>> lights.on()
>>> lights.off()
>>> lights.blink()
```

3. Versuche nun, die LED mit unterschiedlichen Geschwindigkeiten blinken zu lassen (die beiden Zahlen sind die **ein-Zeit** und die **aus-Zeit**):
    
    ```python
>>> lights.blink(2, 2)
>>> lights.blink(5, 5)
>>> lights.blink(0.1, 0.1)
```

4. Versuche nun, alle drei LEDs mit unterschiedlichen Geschwindigkeiten blinken zu lassen:
    
    ```python
>>> lights.red.blink(1, 1)
>>> lights.amber.blink(2, 2)
>>> lights.green.blink(3, 3)
```