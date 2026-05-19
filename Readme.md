# AdventureWorks BI Dashboard | SQL + Power BI

## Описание проекта

Интерактивный аналитический дашборд для компании AdventureWorks (2001–2004). 
Проект демонстрирует полный цикл аналитики: от загрузки данных в БД до 
визуализации финансовых метрик и сегментации клиентов.

## Источник данных

- **База данных:** AdventureWorks (Microsoft), адаптированная для MySQL
- **Источник:** [tapsey/AdventureWorksMYSQL](https://github.com/tapsey/AdventureWorksMYSQL)
- **Развертывание:** локальная установка MySQL + DBeaver

## Структура данных

| Таблица | Строки | Описание |
|---------|--------|----------|
| SalesOrderHeader | 31 465 | Заголовки заказов |
| SalesOrderDetail | 121 317 | Строки заказов |
| Product | 504 | Продукты |
| Customer | 19 185 | Клиенты |
| SalesTerritory | 10 | Территории продаж |

## Технологический стек

| Компонент | Инструмент |
|-----------|------------|
| База данных | MySQL 8.0 |
| SQL-запросы | CTE, оконные функции, JOIN, агрегаты |
| ETL / моделирование | Power BI (Import mode) |
| Визуализация | Power BI Desktop |
| Дизайн | Кастомная тема |

## Страницы дашборда

### 1. Executive Summary
- KPI: Revenue, Gross Profit, Operating Profit
- Динамика выручки и прибыли по годам (2001–2004)
- Разбивка Online vs Offline

### 2. Product & Margin Analysis
- Топ-20 убыточных продуктов
- Анализ по категориям: Bikes, Components, Clothing, Accessories
- Инсайты по ассортименту

### 3. Territory & Sales Team
- Маржа по 10 территориям
- Эффективность 11 менеджеров продаж

### 4. Customer Segments (RFM)
- RFM-сегментация: Champions, Loyal, At Risk, Lost и др.
- Стратегия удержания по сегментам

### 5. P&L Financial Waterfall
- Водопад прибыли: Revenue → COGS → Gross Profit → Freight → Tax → Operating Profit
- Диагностика операционного убытка

## Ключевые выводы

| Метрика | Значение |
|---------|----------|
| Total Revenue | $109,85 млн |
| Gross Profit | $9,37 млн (8,53%) |
| **Operating Profit** | **−$4,00 млн (−3,64%)** |
| Online Revenue | 27% выручки, 40% маржа |
| Offline Revenue | 73% выручки, −2,88% маржа |

## Файлы проекта

| Путь | Описание |
|------|----------|
| `data/` | SQL-скрипты для создания таблиц (не включены, см. источник) |
| `SQL_scripts_BI.txt` | Основные скрипты |
| `powerbi/AdventureWorks.pbix` | Исходный файл дашборда |
| `AdventureWorks_SQL` | Дашборд в PDF |
| `README.md` | Описание проекта |
