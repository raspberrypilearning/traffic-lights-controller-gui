## Blinken Sie die LEDs

1. Öffne Python 3 aus dem Hauptmenü.

2. Geben Sie die folgenden Befehle einzeln in die Python-Shell ein und beobachten Sie die LED:
    
    (Bitte nicht die Chevrons eingeben `>>>`)
    
    ```python
>>> von gpiozero import TrafficLights>>> Lichter = TrafficLights (22, 27, 17)>>> lights.on ()>>> lights.off ()>>> lights.blink ()
```

3. Versuchen Sie nun, die LED mit unterschiedlichen Geschwindigkeiten zu blinken (die beiden Zahlen sind **on time** und **off time**):
    
    ```python
>>> lights.blink (2, 2)>>> lights.blink (5, 5)>>> Lichter.blink (0.1, 0.1)
```

4. Versuchen Sie nun, alle drei LEDs mit unterschiedlichen Geschwindigkeiten zu blinken:
    
    ```python
>>> lights.red.blink (1, 1)>>> lights.amber.blink (2, 2)>>> lights.green.blink (3, 3)
```