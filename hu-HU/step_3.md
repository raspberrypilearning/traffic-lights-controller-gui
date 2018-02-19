## Vigye a LED-eket

1. Nyissa meg a Python 3-at a főmenüből.

2. Adja meg a következő parancsokat, egyenként, a Python héjba, és figyelje a LED-et:
    
    (ne írja be a chevrons `>>>`)
    
    ```python
>>> a gpiozero importtól TrafficLights>>> lights = TrafficLights (22, 27, 17)>>> lights.on ()>>> lights.off ()>>> lights.blink ()
```

3. Most próbálja meg villogni a LED-et különböző sebességgel (a két szám: 123_8_0_321 | az időben</strong> és **kikapcsolási idő**):
    
    ```python
>>> lights.blink (2, 2)>>> lights.blink (5, 5)>>> lights.blink (0,1, 0,1)
```

4. Most próbálja meg villogni mindhárom LED-et különböző sebességgel:
    
    ```python
>>> lights.red.blink (1, 1)>>> lights.amber.blink (2, 2)>>> lights.green.blink (3, 3)
```