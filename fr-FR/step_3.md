## Clignote les LED

1. Ouvrez Python 3 depuis le menu principal.

2. Entrez les commandes suivantes, une par une, dans le shell Python et observez le voyant:
    
    (ne pas taper les chevrons `>>>`)
    
    ```python
>>> à partir de gpiozero import TrafficLights>>> feux = feux de circulation (22, 27, 17)>>> lights.on ()>>> lights.off ()>>> lights.blink ()
```

3. Maintenant, essayez de faire clignoter la LED à différentes vitesses (les deux chiffres sont **à l'heure** et **off time**):
    
    ```python
>>> lights.blink (2, 2)>>> lights.blink (5, 5)>>> lights.blink (0.1, 0.1)
```

4. Essayez maintenant de faire clignoter les trois voyants à des vitesses différentes:
    
    ```python
>>> lights.red.blink (1, 1)>>> lights.amber.blink (2, 2)>>> lights.green.blink (3, 3)
```