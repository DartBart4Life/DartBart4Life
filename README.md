<!---
DartBart4Life/DartBart4Life is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

# Project Title

Проект контроллера газового котла по протоколу OpenTHERM с возможностью интеграции в системы умных домов.

# Technical Specification

Контроллер умного дома должен:
- уметь управлять газовым котлом по протоколу OpenTHERM;
- иметь радиоканал 2.4 ГГц для связи с системой умного дома (протоколы zigbee или Wi-Fi);
- иметь возможность автономной работы без системы умного дома по внешнему датчику температуры;
- иметь возможность интеграции в систему умного дома (tuya, yandex, google home);
- иметь возможность управлять сухими контактами или релейными выходами;
- иметь индикацию состояния (дисплей или светодиод);

# Project Description

Обновить описание
## GPIO
Display:
- GPIO3 - SPI_MOSI
- GPIO2 - SPI SLK
- GPIO7 - SPI CS
- GPIO12 - DC
- GPIO13 - RESET
- GPIO10 - PWM-LCD blacklight - подсветка дисплея, можно подать лог 1 для свечения в полную яркость, можно плано изменять ярокость изменяя скважность шима.
  
Sensos:
- GPIO4 - i2c SDA 
- GPIO5 - i2c SCL
  
USB:
- GPIO18 - USB D+
- GPIO19 - USB D-

Buttons:
- GPIO0
- GPIO1

Relay output:
- GPIO6

UART0 (OpenTHERM)

## Support

For support, text in git of autors or join our Slack channel.

## Authors
- [@EgorKraev](https://github.com/EgorKraev)

- [@DartBart4Life](https://www.github.com/DartBart4Life)


## Tech Stack

**Client:** HTML

**Server:** С



- 👋 Hi, I’m @DartBart4Life
- 🌱 I’m currently learning c++.
