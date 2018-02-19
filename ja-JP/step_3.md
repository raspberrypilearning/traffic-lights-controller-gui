## LEDをフラッシュする

1. メインメニューからPython 3を開きます。

2. 次のコマンドを1つずつPythonシェルに入力し、LEDを観察します。
    
    （シェブロンを入力しないでください`>>>`）
    
    ```python
>>> gpiozeroからのインポートTrafficLights>>> lights = TrafficLights（22,27,17）>>> lights.on（）>>> lights.off（）>>> lights.blink（）
```

3. 異なる速度でLEDを点滅させてみてください（2つの数字は**123_9_1_321 |と**off時間**）：</p> 
    
    ```python
>>> lights.blink（2、2）>>> lights.blink（5、5）>>> lights.blink（0.1、0.1）
```</li> 

- 3つのLEDを異なる速度で点滅させてみましょう。
    
    ```python
>>> lights.red.blink（1,1）>>> lights.amber.blink（2、2）>>> lights.green.blink（3、3）
```</ol>