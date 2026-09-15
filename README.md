# Albion Multi Tools

Локальная утилита-оверлей для **Albion Online**. Распознаёт текущую зону со скриншота (офлайн OCR), показывает информацию о локации в оверлее, считает фейм и делёжку серебра. Работает без интернета — никакая телеметрия и данные пользователя никуда не отправляются.

## Скачивание

Актуальная версия — на странице [Releases](https://github.com/Skyrisse/AlbionMultiTools/releases). Скачай `AlbionMultiTools_vX.Y.Z.zip`, распакуй и запусти `Albion Multi Tools.exe`.

## Вкладки

### СКАНЕР
- **Сканирование зоны** — по нажатию кнопки мыши (СКМ / ЛКМ / ПКМ / боковые — настраивается) делает скриншот области миникарты, локальный OCR (Tesseract) читает название зоны
- **Оверлей** — Albion-стилизованная панель с иконкой зоны, списком объектов и легендой; автозакрытие, прозрачность, масштаб, смещение по X/Y
- **Фильтры отображения** — сундуки, данжи, объекты, ресурсы, легенда (включаются отдельно)
- **Таймер** — настраиваемое время (м:сс) и горячая клавиша (по умолчанию F9), по истечении — сигнал «ВРЕМЯ!»
- **Логи** — отдельное topmost-окно с последними сканами
- **Маршрут** — окно построения маршрута по названию локации

### КНИГИ ФЕЙМА
- Калькулятор книг фейма T1 / T3–T8 с иконками
- Общий фейм, цель («Нужно») и остаток («Осталось»)
- Значения сохраняются между запусками

### РАСЧЕТЫ
- **Сумма минус %** — быстрый расчёт цены с учётом процента (например, налога)
- **Делёжка** — список отсканированных значений серебра, сумма и деление на N человек

### БИЛДЫ
- Встроенный редактор билдов (порт **Albion Forge**) — работает прямо в приложении, без браузера
- Библиотека билдов и групповых составов (до 20 участников)
- Экипировка: 10 слотов, свапы, качество предмета, выбор способностей
- Характеристики персонажа: HP, энергия, броня, средний IP (владение/спеки = 100)
- Сравнение двух билдов, обмен кодами `AF1.` (совместимы с сайтом), импорт/экспорт `.albion.json`, экспорт PNG
- Билды сохраняются локально в `forge_builds.json`

### АВТОР
- Контакты автора: **Discord: Crulich**, **Albion Online: Crulich** (копирование в один клик)
- **«Уже поддержали»** — окно со списком поддержавших и предметами
- **Обновления** — кнопка проверки + автопроверка при запуске; скачивание с проверкой SHA-256 и самозамена exe (настройки сохраняются)

## Особенности

- **Полностью офлайн** — база зон и OCR в комплекте, интернет нужен только для проверки обновлений (можно отключить)
- **9 языков интерфейса** — EN, RU, PL, UK, KK, ZH, FR, DE, IT
- **Трей** — сворачивание в системный трей
- **Бесплатно** — без лицензий и активаций, просто скачай и пользуйся
- Настройки, позиции окон и введённые данные сохраняются в `config.json`

## Системные требования

- Windows 10/11, 64-bit
- Установленная Albion Online, видимая миникарта

## Контакты

- Discord: **Crulich**
- Albion Online: **Crulich**

## Скриншоты

![Builds](https://raw.githubusercontent.com/Skyrisse/AlbionMultiTools/main/screenshots/tab_builds.png)


![Overlay](https://raw.githubusercontent.com/Skyrisse/AlbionMultiTools/main/screenshots/overlay_outpost.png)
![Overlay zone](https://raw.githubusercontent.com/Skyrisse/AlbionMultiTools/main/screenshots/overlay_zone.png)
![Scanner](https://raw.githubusercontent.com/Skyrisse/AlbionMultiTools/main/screenshots/windows_scanner.png)
![Fame tomes](https://raw.githubusercontent.com/Skyrisse/AlbionMultiTools/main/screenshots/tab_fame.png)
![Calculations](https://raw.githubusercontent.com/Skyrisse/AlbionMultiTools/main/screenshots/tab_calc.png)
![Author](https://raw.githubusercontent.com/Skyrisse/AlbionMultiTools/main/screenshots/tab_author.png)
