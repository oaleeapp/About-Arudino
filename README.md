# About-Arudino
關於Arduino的介紹以及相關學習資源的紀錄

## 什麼是Arduino

  依照[官方網站的介紹](https://www.arduino.cc/en/Guide/Introduction)，Arduino是一塊可以用簡單方式創造原型(prototype)的開源軟體以及硬體。
  可以利用各種感知器(sensor)來感受光線或其他外界變化，或者用按鈕操控，甚至是社群網站的訊息等等方式，來輸入資訊。進而將這些資訊處理或者判斷之後，轉換成輸出，點亮LED燈、驅動馬達或者透過網路傳送訊息。
  你可以將你的想法設定在Arduino板裡面，透過將程式燒錄到在板子上的微控制器(microcontroller)。而使用的[專門的程式語言](https://www.arduino.cc/en/Reference/HomePage)（以[Wiring](http://wiring.org.co)為基礎），以及相對應的[整合開發環境](https://www.arduino.cc/en/Main/Software)（Arduino IDE）來開發相關的程式。
  
  [![Arduino介紹影片](https://img.youtube.com/vi/UoBUXOOdLXY/0.jpg)](https://www.youtube.com/watch?v=UoBUXOOdLXY)
  
  所以簡單的說，他就是一個可程式的數位互動裝置。
  
##### 優點:
  1. 價錢親民：最基本款的Arduino Uno大約400~600台幣就可以買到，由於是開源，所以很多其他廠牌出的板子，品質可能會有差異。[參考購買連結](https://www.taiwaniot.com.tw/shop/mcuboard/arduino/arduino-genuino-uno/) [參考購買連結2](https://www.taiwaniot.com.tw/shop/mcuboard/arduino/arduino-uno-r3-原廠晶片-mega328-atmega16u2-非低價劣質pcb-印刷/)
  2. 跨平台：Arduino IDE支援MacOSX, Linux, Windows。很多微控制器的系統是不支援的。
  3. 開源且可擴充的軟體：Arduino的軟體作為一個開源工具，讓很多資深工程師也可以參與發展。另外也可以透過C++的Library來擴充。也可以透過學習AVR-C語言來直接編輯。
  4. 開源且可擴充的硬體：Arduino的硬體是透過CC方式發佈，所以可以讓其他有經驗的IC設計者進一步改善這個板子。甚至，如果是沒經驗的人可以用麵包板來製作自己的Arduino板。Fun!
  
  
## 硬體：Arduino板

  關於Arduino板的相關規格以及介紹可以在[這裡](https://www.arduino.cc/en/Main/Products)找到。
  而一般初學最一開始使用的是Arduino Uno(美國以外稱Genuino Uno，至於為什麼有兩個名字，可以參考[這篇文章](http://www.makezine.com.tw/make2599131456/arduinoadafruitgenuino))，因為這個板子功能最簡單、價格最親民而且也可以依照需求，加裝不同的[shield](https://www.arduino.cc/en/Main/arduinoShields)。
  另外，也因為有很多[其他廠商開發](http://makerpro.cc/2016/03/whats-more-than-arduino-compatible/)的板子都與Arduino Uno相容，所以學了這個規格之後，很多地方都可以套用，一勞永逸。
  
  簡單的介紹過後，來看一下Uno的規格
  
|項目|規格|
|---|---|
|微控制器|[ATmega328P（8-bit）](http://www.atmel.com/images/Atmel-8271-8-bit-AVR-Microcontroller-ATmega48A-48PA-88A-88PA-168A-168PA-328-328P_datasheet_Complete.pdf)|
|工作電壓|5 V|
|輸入電壓(建議)|7-12 V|
|輸入電壓(限制)|6-20 V|
|數位輸出入接腳(I/O Pins)|14(其中6支腳有提供PWM輸出)|
|PWM數位輸出入接腳|6|
|類比輸入接腳|6|
|輸出入直流電流|20 mA|
|3.3V接腳直流電流|50 mA|
|Flash Memory|32 KB(ATmega328P 其中0.5KB作為啟動程式使用)|
|SRAM|2 KB(ATmega328P)|
|EEPROM|1 KB(ATmega328P)|
|時脈速度|16 MHz|
|長度|68.6 mm|
|寬度|53.4 mm|
|重量|25 g|

  如果要比較的話

  以大小來說，不能做為穿戴式裝置使用。
  以速度來說，16MHz跟其他的晶片規格比起來，算是很慢，
  另外他的微控制器是8-bit，所以就本身能力來說，並不是特別突出。

  不過，要用來開發簡單的原型(Prototype)產品或者是互動裝置，其實已經非常足夠，而且有清楚的腳位標示。以及基本的數位類比的輸出入。已經可以完成大部分的操作，另外在接腳部分都可以簡單地用杜邦線或一般的線連接，只要有一塊麵包板就可以很快地利用官方提供的教學上手。

  另外，連接電腦可以直接利用USB來操作，直接可以提供電源以及燒錄。如果要單純提供電源，也可以利用電池或變壓器接交流電。

  其他相關資訊可以查看[官方網站](https://www.arduino.cc/en/Main/ArduinoBoardUno)




好了，讓我們來看看他的IDE以及軟體吧。

## 軟體 Arduino IDE and Programming Language

  [相關程式語言Documents](https://www.arduino.cc/en/Reference/HomePage)
  
  如果你想要學習如何使用Arduino，可以先前往[這裡下載IDE](https://www.arduino.cc/en/Main/Software)。
  安裝之後，會看到一個像下面這個畫面：
  
  ![IDE圖片](https://www.arduino.cc/en/uploads/Guide/Arduino1Blink.png)
  
  你可以在[這裡找到相關的官方教學](https://www.arduino.cc/en/Tutorial/BuiltInExamples)，甚至詳細地告訴你要如何接線。
  
  或者可以觀看Arduino Starter Kit的相關影片教學（老師是其中一個Arduino的創辦人）
  [![Arduino教學影片](https://img.youtube.com/vi/2X8d_r0p92U/0.jpg)](https://www.youtube.com/watch?v=2X8d_r0p92U&list=PLEFD8868A15D860D7)

  關於[IDE的教學](https://www.arduino.cc/en/Guide/Environment#toc7)可以從這邊看。
  
  不過有一些我每次都會check的地方，或者一些觀念會在以下說明。
  
####  Sketch
  每一個Arduino的文檔都是一個sketch，檔案格式為.ino。
  每個sketch專案裡面可以分為五個部分：
  1. 最頂端的註釋：使用註解的方式對於這個案子的題目做一些簡單的介紹。
  2. 變數宣告：在註解下面，會引用其他的library以及做一些基本的變數還有常數的宣告。
  3. setup()：只會在最一開始執行一次的程式，是程式最先執行的地方，可以在此設定一些基本狀態，以及只需要執行一次的程式。
  4. loop()：顧名思義，這個迴圈會持續的不停循環，主要的邏輯會放在這個函式內，可以在這邊讀取輸入的值，以及利用輸出操作不同的致動器(Actuator)。也可以使用Delay等等函式來決定速度。
  5. 副程式：可以將較複雜或者會重複使用的邏輯，另外寫成函式。
  
PS：也可以把副程式另外寫在同一個資料夾下的sketch內，利用新增分頁的方式就可以開啟一個編輯區域。

#### 檢查Tools/Board跟Tools/Port是否有連結
  在每次開始用之前，檢查是否有正確連結Arduino板，以及是否有在Tools/Board裡面選擇正確的板子。另外為了要使用待會兒會介紹的serial monitor，要確定Tools/Port是否有正確選擇到目前USB接到的port。
  若沒有看到相對應的板子，或者使用其他廠商開發的板子，可以在Board Manager裡面尋找，或者在該廠商的網站確認如何下載。
  
#### Verify 和 Upload
  這就有點像是Verify不會把程式燒到板子上，但會確認是否能夠順利compile。Upload會先做verify再將程式燒錄至Arduino板？
  
#### Serial Monitor
  可以利用`Serial.begin(9600);`等等相關的語法，來讓讀取到的資訊顯示在電腦上。要打開serial monitor可以點擊介面右上角的放大鏡。就可以打開。
  進一步了解，請閱讀[Serial](https://www.arduino.cc/en/Reference/Serial)
  
#### Example 範例
  如果你已經有閱讀他們的教學，應該可以很輕易的找到相對應的範例程式。在File/Examples裡面可以找到你要的程式。
  可以好好利用它的[官方教學](https://www.arduino.cc/en/Tutorial/BuiltInExamples)，真的非常容易操作：）
  
  
  
  ------
  以上就是關於Arduino以及相關硬體及軟體介面的相關介紹，歡迎分享。
  
  若有發現錯誤的地方也請通知我。
