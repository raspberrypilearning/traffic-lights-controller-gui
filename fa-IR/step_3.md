## چراغ های فلش

1. پایتون 3 را از منوی اصلی باز کنید.

2. دستورات زیر را به صورت یک به یک در پوسته پایتون وارد کنید و LED را مشاهده کنید:
    
    (شویرون را تایپ نکنید `>>>`)
    
    ```python
>>> از gpiozero import TrafficLights>>> چراغ = TrafficLights (22، 27، 17)>>> lights.on ()>>> lights.off ()>>> lights.blink ()
```

3. در حال حاضر سعی کنید چشمک زدن LED در سرعت های مختلف (دو عدد هستند **در زمان** و **خاموش زمان**):
    
    ```python
>>> lights.blink (2، 2)>>> lights.blink (5، 5)>>> lights.blink (0.1، 0.1)
```

4. در حال حاضر تمام سه LED با سرعت های مختلف فلاش بزنید:
    
    ```python
>>> lights.red.blink (1، 1)>>> lights.amber.blink (2، 2)>>> lights.green.blink (3، 3)
```