# StickWatch
A smart watch based on M5Stick of ESP32

https://item.taobao.com/item.htm?id=581055502939



Use ESP-idf + Arduino to build this project with configuration:
M5Stack-Core-ESP32, QIO, 80MHz, No OTA (Large APP), 921600, Verbose

StickWatch.ino 파일의 경로

<img src="images/path.jpg">

### StickWatch.ino 컴파일전에 다음과 같은 설정이 필요함.

**1. Arduino IDE에서 Tools -> Partition Scheme -> Large App No OTA를 선택**

**2. 다음의 라이브러리의 설치가 필요함**
- Wifi
<img src="images/library_wifi.png">
- ArduinoJson (6.2.0-beta as local dependancy)
<img src="images/library_arduinojson.png">

**3. WIFI 설정**

시간을 올바르게 표시하려면 WIFI를 구성해야 함.

config.h 파일을 열고 라인 5와 6을 수정하고 wifi 계정과 암호로 변경하십시오.

```arduino
// user configurable variables start
const char* BUILTIN_WIFI_SSID      = "Your WIFI ssid";
const char* BUILTIN_WIFI_PASSWORD  = "********";
```
그런 다음 StickWatch.ino을 컴파일하고 다운로드.

### 주의

스틱에 해당 하드웨어 회로가 지원되지 않으므로 스틱에 표시된 온도 및 전압 값을 프로그래밍 할 수 없으면 사용할 수 없습니다.
