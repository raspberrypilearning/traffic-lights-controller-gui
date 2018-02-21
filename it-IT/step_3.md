## Flash i LED

1. Apri Python 3 dal menu principale.

2. Inserisci i seguenti comandi, uno alla volta, nella shell Python e osserva il LED:
    
    (non digitare le frecce `>>>`)
    
    ```python
>>> da gpiozero import TrafficLights>>> lights = TrafficLights (22, 27, 17)>>> lights.on ()>>> lights.off ()>>> lights.blink ()
```

3. Ora prova a lampeggiare il LED a velocità diverse (i due numeri sono **in orario** e **tempo di spegnimento**):
    
    ```python
>>> lights.blink (2, 2)>>> lights.blink (5, 5)>>> lights.blink (0.1, 0.1)
```

4. Ora prova a lampeggiare tutti e tre i LED a velocità diverse:
    
    ```python
>>> lights.red.blink (1, 1)>>> lights.amber.blink (2, 2)>>> lights.green.blink (3, 3)
```