# Лабораторна робота №1


## Аналіз якості програмного продукту. Виявлення та документування аномалій


**Виконав:** Волик Денис
**Група:** 6.1214-c2
**Дата виконання:** 14.10.2026



## Тестовий об’єкт



SauceDemo

https://www.saucedemo.com/



## Тестове середовище


- Операційна система: Windows 11
- Браузер: Google Chrome
- Дата тестування: 14.10.2026



## Базовий сценарій
За допомогою облікового запису `standard_user` було перевірено
авторизацію, перегляд каталогу, додавання товару до кошика та
оформлення замовлення.
Основний сценарій було завершено успішно.


## Виявлені аномалії
- №1
- Користувач: performance_glitch_user
- Короткий опис: Довго логінe цього користувача.
- Severity: Medium
- Priority: Medium
- Issue: [Link](https://github.com/csylwip/software-quality/issues/1#issue-5842144262)
#
- №2
- Користувач: problem_user
- Короткий опис: Цей користувач бачить картинки собак замість картинок продуктів.
- Severity: High
- Priority: Medium
- Issue: [Link](https://github.com/csylwip/software-quality/issues/2#issue-5842180494)
#
- №3
- Користувач: problem_user
- Короткий опис: У користувача не відкривається сторінка Sauce Labs Fleece Jacket.
- Severity: Medium
- Priority: Medium
- Issue: [Link](https://github.com/csylwip/software-quality/issues/3#issue-5842214049)
## Висновок

Було вивчено спосіб створення Github Issues та пояснення дефектів.
