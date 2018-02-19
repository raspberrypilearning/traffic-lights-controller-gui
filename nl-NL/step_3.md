## Flits de leds

1. Open Python 3 vanuit het hoofdmenu.

2. Voer de volgende commando's één voor één in de Python-shell in en observeer de LED:
    
    (typ niet de chevrons `>>>`)
    
    ```python
>>> from gpiozero import TrafficLights>>> lights = TrafficLights (22, 27, 17)>>> lights.on ()>>> lights.off ()>>> lights.blink ()
```

3. Probeer nu de LED met verschillende snelheden te knipperen (de twee nummers zijn **op tijd** en **uitschakeltijd**):
    
    ```python
>>> lights.blink (2, 2)>>> lights.blink (5, 5)>>> lights.blink (0.1, 0.1)
```

4. Probeer nu alle drie de LED's met verschillende snelheden te knipperen:
    
    ```python
>>> lights.red.blink (1, 1)>>> lights.amber.blink (2, 2)>>> lights.green.blink (3, 3)
```