# Albion Zone Checker

Оверлей для Albion Online: распознаёт название зоны на миникарте (OCR) и
показывает поверх игры карту зоны с краткой информацией.

## Требования

- Python 3.12+
- [Tesseract OCR](https://github.com/UB-Mannheim/tesseract/wiki) (по умолчанию
  ищется в `C:\Program Files\Tesseract-OCR\tesseract.exe`)
- Зависимости: `pip install -r requirements.txt`

## Запуск

```
python app.py
```
или `run.bat`

## Как работает

1. По нажатию средней кнопки мыши (`trigger_button`) захватывается область
   `minimap_region` из `config.json`. Авто-сканирования нет — только по клику
   или по кнопке «Тест скан».
2. Изображение переводится в HSV, выделяется светлый текст, Tesseract
   распознаёт слова.
3. Слова (одиночные и группы до 3 подряд) сверяются с базой
   `data\avalon_zones.json` через rapidfuzz (`fuzz.ratio` × вес покрытия).
4. При score ≥ `min_match_score` показывается оверлей-панель как в игре:
   пергамент (`data\background.png`), бейдж тира/хайдаута, ряды иконок из
   `data\icons\` — сундуки, данжи, кемпы, статические данжи, замки/клеймы/
   порталы и ресурсы с подписями вида `T7★` (★ — премиум-ресурс).
   Повторное срабатывание на ту же зону блокируется на
   `same_zone_cooldown_s` секунд.

## Конфиг (`config.json`)

| Ключ | Описание |
|---|---|
| `minimap_region` | Координаты области миникарты `{x, y, width, height}` |
| `poll_interval_ms` | Интервал авто-сканирования |
| `min_match_score` | Минимальный балл совпадения (0–100) |
| `same_zone_cooldown_s` | Кулдаун повторного показа той же зоны |
| `overlay_auto_close_ms` | Через сколько мс закрыть оверлей |
| `overlay_alpha`, `overlay_scale`, `overlay_x/y_offset` | Вид и позиция оверлея |
| `click_mode_enabled`, `trigger_button` | Скан по клику (`middle`, `right`, …) |
| `min_scan_interval_ms` | Минимальный интервал между сканами |

## Что не реализовано (в отличие от оригинала)

- Распознавание таймеров порталов (ONNX-модель `timer_ctc.onnx` скопирована в
  `data\`, но не используется)
- Телеметрия и интеграция с portaler (токены в конфиг не копировались)
- Настройка области миникарты через GUI — правится в `config.json`
