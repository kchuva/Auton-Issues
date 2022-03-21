# Auton-Issues
### Список интересных задач
| ID | Описание |
| --- | --- |
| [15419](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=15419) | эксперименты с BLE драйверами, стеком |
| [15686](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=15686) | проработка возможности использования донгла nRF52840 Dongle, создание прошивки CDC ACM USB |
| [15178](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=15178) | найдена проблема с шагами After Build при сборке проекта через TFS Agent |
| [15523](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=15523) | описание интересных моментов, которые приводили к повышенному потреблению nRF52 |
| [13910](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=13910) | ошибка FDS при частой записи во время работы сборщика мусора, что приводило в итоге к ошибке пейринга |
| [13326](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=13326) | ошибка в модуле equeue, связанная с переполнением внутреннего счетчика времени |
| [13619](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=13619) | ошибка при выполнении Discover characteristics в драйвере BTWrapper_Autograph, связано с добавлением нового атрибута в GATT-таблицу сервиса Автон (**_нужно проверить как новый стек отрабатывает эту ситуацию_**) |
| [15307](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=15307) | подробно описана проблема отставания времени в реалиазации сетевого сервера LoRaWAN GotthardP |
| [14899](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=14899) | проблема запуска прошивки в Release-версии шлюза (задействован вывод RESET в бутлоадере для платы, на которой этот вывод подключен как GPIO) |
| [15400](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=15400) | описана проблема сетевого сервера ChirpStack по поддержке спецификации 1.0.3 |
| [15972](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=15972) | ошибка записи во внутреннюю flash-память |
| [15991](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=15991) | ошибка передачи данных в динамографе |
| [16282](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=16282) | ошибка передачи данных в динамографе |
| [15137](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=15137) | ОПИ шлюза в ЭР-Телеком, описание ошибок парсинга на стороне сервера и снова проблема ChirpStack и версии 1.0.3 спецификации |
|  |  |
| [13660](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=13660) | ошибка работы GSM модема в A114-20 (проблема на момент работы над задачей была закрыта, но воспроизводится в других устройствах, причина проблемы не найдена - есть связанная задача 13042) |
| [13042](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=13042) | ошибка функционирования модема GSM SIM800 в A515-20 (на текущий момент причина не найдена, есть связанная задача 13660) |
| [13246](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=13246) | нестабильная работа модема GSM SIM800 в тесте самодиагностики (связана с задачами 13660, 13042) |
| [13131](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=13131) | разработан механизм приема данных по UART через DMA, но пока не используется |
| >13185 | |

### Неразрешенные проблемы (не воспроизводятся)
| ID | Описание |
| --- | --- |
| [14414](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=14414) | зависание в методе отправки данных по SPI |
| [13454](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=13454) | невозможно подключиться к датчику по BLE после обновления прошивки |
| [14848](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=14848) | ЭрТелеком, Chirpstark - проблема отстутствия передачи данных по LoRaWAN |
| [10890](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=10890) | Сибур - периодическая остановка передачи данных по LoRaWAN |

### Интересные ссылки
1. Почему в Keil нельзя виртуальные деструкторы и no-heap одновременно\
https://stackoverflow.com/questions/13445147/keil-virtual-or-protected-destructor-and-heap
2. Реализация startup-кода в библиотеке newlib-arm от GNU GCC на примере nRF52840\
https://embeddedartistry.com/blog/2019/04/17/exploring-startup-implementations-newlib-arm/
3. Официальный репозиторий Nordic Semiconductor\
https://github.com/NordicSemiconductor
4. Дополнительный репозиторий для вспомогательных проектов\
https://github.com/NordicPlayground

### Исправление возможных проблем
#### Потребление
1. Описание аномалии высокого потребления при работе с таймерами\
https://infocenter.nordicsemi.com/topic/errata_nRF52832_Rev3/ERR/nRF52832/Rev3/latest/anomaly_832_78.html
2. Инструкция по минимизации потребления для чипов nRF\
https://devzone.nordicsemi.com/f/nordic-q-a/1657/how-to-minimize-current-consumption-for-ble-application-on-nrf51822#reply-5187

#### Зависание/перезагрузка/HardFault
1. Проверить размер используемого стека
2. Обращение к нулевому объекту
3. Разыменовывание указателя по невыровненной памяти

#### Разрыв соединения Bluetooth
1. Проверить выставленную точность кварца (связанная задача [13277](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=13277))
2. Уточнить этап на котором происходит разрыв соединения
3. Проверить параметры подключения, особенно Latency (связанная задача [13264](http://atfs16:8080/tfs/DefaultCollection/A/_workitems?_a=edit&id=13264))

##### Разрыв соединения с кодом 0x28 (BLE_HCI_INSTANT_PASSED)
https://devzone.nordicsemi.com/f/nordic-q-a/80082/eliminate-ble_hci_instant_passed-0x28-ble-disconnection \
https://devzone.nordicsemi.com/f/nordic-q-a/29054/handling-connection-parameter-update-request-from-central
