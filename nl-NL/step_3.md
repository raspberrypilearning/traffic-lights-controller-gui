## Laat de leds knopperen

1. Open vanuit het hoofdmenu Python 3.

2. Voer de volgende commando's in de Python-shell één voor één in en observeer de LED's:
    
    (typ de chevrons `>>>` niet in)
    
    ```python
>>> from gpiozero import TrafficLights
>>> lights = TrafficLights(22, 27, 17)
>>> lights.on()
>>> lights.off()
>>> lights.blink()
```

3. Probeer nu de LED's met verschillende snelheden te laten knipperen, de twee nummers zijn **on time** (tijd aan) en **off time**( tijd uit):
    
    ```python
>>> lights.blink(2, 2)
>>> lights.blink(5, 5)
>>> lights.blink(0.1, 0.1)
```

4. Probeer nu alle drie de LED's met verschillende snelheden te laten knipperen:
    
    ```python
>>> lights.red.blink(1, 1)
>>> lights.amber.blink(2, 2)
>>> lights.green.blink(3, 3)
```