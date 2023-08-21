# ADR3. Предметная область

| Актуальное | Принято 24.07.23                          |
|------------|-------------------------------------------|
| Участники  | Бутаков М.В.                              |
| Изменения  | 21.07.23 - Создано<br/>21.07.24 - Принято |

Задача: выявить домены предметной области

<!-- TOC -->
* [ADR3. Предметная область](#adr3-предметная-область)
  * [Группировка сценариев по затронутым объектам](#группировка-сценариев-по-затронутым-объектам)
    * [Пользователи](#пользователи)
    * [Игровые комнаты](#игровые-комнаты)
    * [Обучение](#обучение)
    * [Контент книг, сеттингов, приключений, хоумбрю](#контент-книг-сеттингов-приключений-хоумбрю)
    * [Подсказки](#подсказки)
    * [Состояние объектов кампании](#состояние-объектов-кампании)
    * [Генераторы](#генераторы)
    * [Персонажи](#персонажи)
    * [Данные прохождения](#данные-прохождения)
  * [Связи](#связи)
<!-- TOC -->

## Группировка сценариев по затронутым объектам

Оранжевым выделены критичные сценарии с повышенными требованиями

### Пользователи

![](svg/chart/domain/user.svg)

### Игровые комнаты

![](svg/chart/domain/room.svg)

### Обучение

![](svg/chart/domain/learn.svg)

### Контент книг, сеттингов, приключений, хоумбрю

**Особенности**: данные меняются редко, и практически никогда - во время партии

![](svg/chart/domain/content.svg)

### Подсказки

**Особенности**: значительный объем входных данных при получении подсказок, практически все запросы можно считать
уникальными.

![](svg/chart/domain/hint.svg)

### Состояние объектов кампании

**Связи**: с контентом книг, сходные структуры
**Особенности**: данные меняются часто, один и тот же "слепок" данных по состоянию объектов в течение 3-5 секунд может
быть применим ко всем участникам игровой комнаты

![](svg/chart/domain/object.svg)

### Генераторы

**Связи**: с состоянием объектов в кампании, генерируют объекты в компании

![](svg/chart/domain/generator.svg)

### Персонажи

**Связи**: с состоянием объектов в кампании, герои - один из объектов в компании

![](svg/chart/domain/hero.svg)

### Данные прохождения

**Связи**: с состоянием объектов в кампании, записи о событиях в прохождении связаны с множеством объектов в компании

![](svg/chart/domain/campaign.svg)

## Связи

![](svg/chart/domains.svg)