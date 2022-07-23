# Получение золота из руды
## Описание проекта
Некоторая компания разрабатывает решения для эффективной работы промышленных предприятий. Требуется построить модель, которая будет прогнозировать коэффициент восстановления золота из золотосодержащей руды, при этом доступны данные с параметрами добычи и очистки.

**Цели проекта:**
1. Подготовить данные.
2. Провести исследовательский анализ данных.
3. Построить и обучить модель для предсказания коэффициента восстановления золота из руды.

## Описание данных
Предоставлены данные с параметрами добычи и очистки на каждом этапе производства. 
### Технологический процесс
* `Rougher feed` — исходное сырье
* `Rougher additions` (или reagent additions) — флотационные реагенты: *Xanthate* — ксантогенат (промотер, или активатор флотации),
*Sulphate* — сульфат (на данном производстве сульфид натрия),
*Depressant* — депрессант (силикат натрия);
* `Rougher process` (англ. «грубый процесс») — флотация;
* `Rougher tails` — отвальные хвосты;
* `Float banks` — флотационная установка;
* `Cleaner process` — очистка;
* `Rougher Au` — черновой концентрат золота;
* `Final Au` — финальный концентрат золота.
### Параметры этапов
* `air amount` — объём воздуха;
* `fluid levels` — уровень жидкости;
* `feed size` — размер гранул сырья;
* `feed rate` — скорость подачи.
### Наименование признаков
Признаки именуются следующим образом:
`[этап].[тип_параметра].[название_параметра]`
Возможные значения для блока `[этап]`:
* `rougher` — флотация;
* `primary_cleaner` — первичная очистка;
* `secondary_cleaner` — вторичная очистка;
* `final` — финальные характеристики.
Возможные значения для блока `[тип_параметра]`:
* `input` — параметры сырья;
* `output` — параметры продукта;
* `state` — параметры, характеризующие текущее состояние этапа;
* `calculation` — расчётные характеристики.
Пример: `rougher.input.feed_ag` — размер гранул серебра перед флотацией.

## Инструменты
`python`, `pandas`, `matplotlib`, `numpy`, `scikit-learn`, `исследовательский анализ данных`