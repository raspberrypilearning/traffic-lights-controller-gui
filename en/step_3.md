## Flash the LEDs

1. Open Python 3 from the main menu.

1. Enter the following commands, one-by-one, into the Python shell, and observe the LED:

  (do not type the chevrons `>>>`)

    ```python
    >>> from gpiozero import TrafficLights
    >>> lights = TrafficLights(22, 27, 17)
    >>> lights.on()
    >>> lights.off()
    >>> lights.blink()
    ```

1. Now try blinking the LED at different speeds (the two numbers are (**on time** and **off time**):

  ```python
  >>> lights.blink(2, 2)
  >>> lights.blink(5, 5)
  >>> lights.blink(0.1, 0.1)
  ```

1. Now try flashing all three LEDs at different rates:

    ```python
    >>> lights.red.blink(1, 1)
    >>> lights.amber.blink(2, 2)
    >>> lights.green.blink(3, 3)
    ```
