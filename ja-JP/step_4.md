## GUIの作成

1. 新しいウィンドウを開き、保存します。 これで、シェル内で直接ではなく、このファイルにコードを記述します。

2. 赤色LEDをオンにするGUIボタンを作成します。
    
    ```python
guizeroからの読み込みgpiozeroからのApp、Text、PushButtonからの読み込みTrafficLightsのlight = TrafficLights（22,27,17）app = App（）PushButton（app、command = lights.red.on、text = "on"）app.display（）
```

![](images/guizero-1.png)

3. 赤いLEDを消すには、テキストラベルと2番目のボタンを追加します。
    
    ```python
PushButton（app、command = lights.red.off、text = "off"）テキスト（app、 "Red"）PushButton（app、command = lights.red.on、text = "on"）
```

![](images/guizero-2.png)

4. 今度はあなたのアプリに名前をつけ、グリッドレイアウトを使用してください：
    
    ```python
（アプリケーション、コマンド= red.on、テキスト= "オ​​ン"、グリッド= "グリッド"）テキスト（アプリケーション、 "赤"、グリッド= [0、0] [0、1]）PushButton（app、command = red.off、text = "off"、grid = [0、2]）
```

![](images/guizero-3.png)