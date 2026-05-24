# AdventureWorks BI Dashboard | SQL + Power BI

## Описание проекта

Интерактивный аналитический дашборд для компании AdventureWorks (2001–2004). 
Проект демонстрирует полный цикл аналитики: от загрузки данных в БД до 
визуализации финансовых метрик, сегментации клиентов и what-if сценариев.

## Источник данных

- **База данных:** AdventureWorks (Microsoft), адаптированная для MySQL
- **Источник:** [tapsey/AdventureWorksMYSQL](https://github.com/tapsey/AdventureWorksMYSQL)
- **Развертывание:** локальная установка MySQL + DBeaver

## Язык
Дашборд построен на английском языке из-за англоязычной исходной базы данных 
(названия продуктов, категории, территории).

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
- KPI: Revenue, Gross Profit, Operating Profit, Operating Margin %
- Динамика выручки и прибыли по годам (2001–2004)
- Combo chart: Revenue + Profit + Margin % с двумя осями
- Инсайты на английском

### 2. Product & Margin Analysis
- Таблица продуктов с conditional formatting
- Цветовая маркировка: 🔴 Critical loss 🟡 Unprofitable 🟢 Profitable
- Фильтрация по категориям (кнопки): Accessories, Bikes, Clothing, Components
- Stacked bar: структура маржи по категориям

### 3. Territory & Sales Team
- Маржа по 10 территориям с target line (средняя маржа)
- Цветовое кодирование: зелёный (плюс) / красный (минус)
- Таблица менеджеров с сортировкой по марже
- Инсайты на английском

### 4. Customer Segments (RFM)
- RFM-сегментация: Champions, Loyal, At Risk, Lost и др.
- Combo chart: Customer Count + Avg Bill по сегментам
- Инсайты на английском

### 5. P&L Financial Waterfall
- Водопад прибыли: Revenue → COGS → Gross Profit → Freight → Tax → Operating Profit
- What-if сценарии:
  - Tax reduction % (0–50%)
  - Price increase % (0–20%)
- Интерактивный расчёт Adjusted Operating Profit
- Инсайты на английском

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
| `dax_measures.txt` | DAX-меры |
| `powerbi/AdventureWorks.pbix` | Исходный файл дашборда |
| `AdventureWorks_SQL` | Дашборд в PDF |
| `README.md` | Описание проекта |