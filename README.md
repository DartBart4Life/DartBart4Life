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

Контроллер газового котла на микросхеме cc2530 ([datasheet](https://www.newbitsiot.com/wp-content/uploads/2022/03/CC2530-Datasheet.pdf)) от Texas Instrumets, эта микросхема является системой на кристале и включает в себя 2.4-GHz IEEE802.15.4-совместимый радиомодуль и ядро intel 8051 ([о ядре](https://ru.wikipedia.org/wiki/Intel_8051)). Микросхема немного устаревшая, но на рынок завален китайскими копиями и огромным количеством складских запасов, что делает ее одной из самых дешевых на рынке. Можно рассмотреть похожие (ESP32-H2, ESP32-C6 (имеет сразу Wi-Fi и zigbee), Nordic nRF52840), но их стоимость выше и доставаемость для открытого проекта довольно таки сложная. 

Для автономного режима, нужно продумать концепцию выноснх датчиков температуры, возможно есть смысл что бы в этом режиме контроллер являлся zigbee-хабом и к нему через веб-интерфейс можно было подключить любые zigbee датчики и по ним регулировать температуру. На борту у контроллера поставить так же цифровой датчик температуры и влажности (BMP280 или AHT20) для большей автономности.

Возможно стоит рассмотреть ethernet-интерфейс (wiznet), в угоду универсальности контроллера и стабильности работы соединения с умным домом (сценарий, когда нет стабильного соединения wi-fi с котельной ввиду удаленности её, и возможно тогда протянуть кабель легче).
## GPIO
- 2 - lcd sclk
- 3 - lcd mosi
- 4 - i2c sda 
- 5 - i2c scl
- 7 - lcd cs
- 12 - lcd dc
- 18 - lcd reset

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
