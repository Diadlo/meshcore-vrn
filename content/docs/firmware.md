+++
title = 'Прошивки'
+++

# Прошивки

{{< firmware-filter tags="компаньон репитер наблюдатель бридж" >}}

<div class="fw-card" data-tags="компаньон репитер">
### Официальная прошивка

Стоковая прошивка, доступная в [онлайн прошивальщике](https://meshcore.co.uk/flasher.html) (ссылка также есть в [гайде для новичков](/docs/beginners)). Исходники — на [GitHub](https://github.com/meshcore-dev/MeshCore).
</div>

<div class="fw-card" data-tags="компаньон репитер">
### Whisper OS

Альтернативная прошивка: [ssaprus.works](https://ssaprus.works/). Исходный код закрыт.
</div>

<div class="fw-card" data-tags="компаньон">
### MeshCore-Solo

Альтернативная прошивка с фокусом на то, чтобы компаньон был самодостаточным устройством. Заточена под работу с джойстиком и e-ink экраном: более удобный интерфейс, комфортная навигация, экранная клавиатура, кастомизируемое меню, дополнительный функционал и тулзы, плюс хорошая энергоэффективность. Начиная с v1.24 появилась русская раскладка клавиатуры. Репозиторий: [github.com/MarekZegare4/MeshCore-Solo](https://github.com/MarekZegare4/MeshCore-Solo).
</div>

<div class="fw-card" data-tags="компаньон репитер">
### Продвинутая прошивка для компаньонов и репитеров (Heltec V3/V4/Xiao S3)

Прошивка на основе [MeshCore-Low-Power-Firmware-For-Heltec-V3-V4](https://github.com/dt267/MeshCore-Low-Power-Firmware-For-Heltec-V3-V4). Поддерживает компаньоны и репитеры на Heltec v3/v4/t096/ Xiao S3. Для компаньонов параметры настраиваются по каналу TerminalCLI. Заявляются повышенное энергосбережение, автоконтроль занятости канала (CAD), вкл/выкл FEM и rxgain, настраиваемые быстрые сообщения с экрана и другие функции.
</div>

<div class="fw-card" data-tags="репитер наблюдатель бридж">
### <span id="observer">Наблюдатель</span> (ObserverPlus)

Сборка наблюдателя с дополнительными фичами и возможностью бриджа по EspNow. Форк от [vbart](https://github.com/vbart). Возможности:

- Контроль занятости канала (CAD): `set cad on/off`.
- Управление усилителем чипа: `set radio.rxgain on/off`.
- Управление FEM: `set radio.fem.rxgain on/off`.
- Выключение репитера через `enterDeepSleep(0)` с кнопки USER (зажать на 3 секунды; включить кнопкой Reset).
- Отображение на дисплее текущего состояния CAD, RxGain, FEM.

Важно: мост по EspNow работает только с такой же прошивкой, т.к. канал EspNow работает на том же частотном слоте, что и Wi-Fi.

Файлы прошивок: [FIRMWARE](https://gitlab.rheostat.crazedns.ru/meshcore_voronezh/observerplus/-/tree/main/FIRMWARE?ref_type=heads). Репозиторий: [observerplus](https://gitlab.rheostat.crazedns.ru/meshcore_voronezh/observerplus).

Примечание: при шитье поверх старой прошивки ObserverPlus используй только файл `_merged.bin` с очисткой FLASH (предварительно сохрани ключ или экспортируй конфигурацию). При обновлении от vbart допустимо обновлять поверх без стирания — файл `firmware.bin`.
</div>

{{< /firmware-filter >}}