## एल. ई. डी. को जलाये

\--- task \---

अपने एल. ई. डी. को निम्नलिखित पिन से कनेक्ट करें:

| एल. ई. डी. | GPIO पिन |
| ---------- |:--------:|
| लाल        |    22    |
| पीला       |    27    |
| हरा        |    17    |

![pi stop connected to gpio 22,27,17 and ground](images/Traffic-Lights-Diagram.png)

\--- /task \---

\--- task \---

Open **Mu** from the main menu. Click the **REPL** icon to open the Python shell.

\--- /task \---

\--- task \---

Python शेल में निम्न आदेशों को एक-एक करके दर्ज करें, और एलईडी का निरीक्षण करें:

```python
from gpiozero import TrafficLights
lights = TrafficLights(22, 27, 17)
lights.on()
lights.off()
lights.blink()
```

\--- /task \---

\--- task \---

अब अलग-अलग गति पर एल. ई. डी. को झिलमिलाने का प्रयास करें (दो संख्याएं हैं **on time** और **off time**):

```python
lights.blink(2, 2)
lights.blink(5, 5)
lights.blink(0.1, 0.1)
```

\--- /task \---

\--- task \---

अब विभिन्न दरों पर तीनों एल. ई. डी. को जलाने की कोशिश करें:

```python
lights.red.blink(1, 1)
lights.amber.blink(2, 2)
lights.green.blink(3, 3)
```

\--- /task \---