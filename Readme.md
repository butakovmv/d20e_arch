# Этот репозиторий

Является итоговой проектной работой для курса Software Architecture от платформы OTUS

### Входящие требования

1. [Бизнес-контекст](req/REQ01-BusinessContext.md)
	1. [Стейкхолдеры](req/REQ01-BusinessContext.md#стейкхолдеры)
	2. [Цели](req/REQ01-BusinessContext.md#цели)
	3. [Потребности](req/REQ01-BusinessContext.md#потребности)
2. [Базовые сценарии](req/REQ02-UseCases.md)
3. [Предметная область](req/REQ03-Domain.md)
4. [Требования](req/REQ04-Limitation.md)
	1. [Структура организации](req/REQ04-Limitation.md#структура-организации)
	2. [Ограничения](req/REQ04-Limitation.md#ограничения)
	3. [Функциональные требования](req/REQ04-Limitation.md#функциональные-требования)
	4. [Нефункциональные требования](req/REQ04-Limitation.md#нефункциональные-требования)
	5. [Архитектурно значимые требования](req/REQ04-Limitation.md#архитектурно-значимые-требования)

### Архитектурные решения
1. [ADR01. Система и ее окружение](adr/ADR01-c4context.md)
	1. [Пользователи](adr/ADR01-c4context.md#роли-пользователей)
	2. [Интеграции](adr/ADR01-c4context.md#внешние-связи)
	3. [Диаграмма](adr/ADR01-c4context.md#решение)
2. [ADR02. Диаграмма контейнеров](adr/ADR02-с4conatiner.md)
	1. [Группировка доменов](adr/ADR02-с4conatiner.md#группировка-доменов)
	2. [Варианты диаграммы](adr/ADR02-с4conatiner.md#варианты-разбиения-на-контейнеры)
	3. [Решение](adr/ADR02-с4conatiner.md#решение)
3. [ADR03. Диаграмма компонентов](adr/ADR03-deploy.md)
	1. [Группировка доменов](adr/ADR03-deploy.md#группировка-доменов)
4. [Диаграммы последовательности](req/SequenceDiagrams.md)
4. [Диаграммы компонентов](adr/ADR03-component.md)
5. Реализация MVP, проведение нагрузочного тестирования, анализ результатов
6. [ADR04. Оптимизация вызовов поиска пользователя](adr/ADR04-optimize-getUser.md)
