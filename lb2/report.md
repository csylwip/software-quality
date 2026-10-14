# Лабораторна робота №2

## Проєктування тестів. Checklist, Test Cases та Decision Table

**Виконав:** Волик Денис Григорович
**Група:** 6.1214-c2
**Дата виконання:** 14.10.2026

## Test Object

SauceDemo — Login
https://www.saucedemo.com/


## Test Conditions

- TCND-01 - успішна авторизація валідного користувача;
- TCND-02 - авторизація з неправильним Username;
- TCND-03 - авторизація з неправильним Password;
- TCND-04 - авторизація з порожнім Username;
- TCND-05 - авторизація з порожнім Password;
- TCND-06 - авторизація заблокованого користувача.

## Checklist

- [ ] Успішна авторизація з валідними даними.
- [ ] Відмова в авторизації з неправильним Username.
- [ ] Відмова в авторизації з неправильним Password.
- [ ] Перевірка порожнього Username.
- [ ] Перевірка порожнього Password.
- [ ] Відмова в авторизації заблокованого користувача.

### TC-LOGIN-01 - Успішна авторизація standard_user

**Type:** Positive

**Preconditions:**
- відкрита сторінка Login;
- користувач не авторизований.

**Test Data:**
- Username: standard_user
- Password: secret_sauce

**Steps:**
1. У поле Username ввести standard_user.
2. У поле Password ввести secret_sauce.
3. Натиснути кнопку Login.

**Expected Result:**

Після введення standard_user і правильного пароля та натискання Login користувач успішно авторизується і переходить на сторінку Products.

**Actual Result:**

Після введення standard_user і правильного пароля та натискання Login відкрилася сторінка Products

**Result:**

Pass

### TC-LOGIN-02 - Авторизація з неправильним Password

**Type:** Negative

**Preconditions:**
- відкрита сторінка Login;
- користувач не авторизований.

**Test Data:**
- Username: standard_user
- Password: wrong_password

**Steps:**
1. У поле Username ввести standard_user.
2. У поле Password ввести wrong_password.
3. Натиснути кнопку Login.

**Expected Result:**

Після введення standard_user і не правильного пароля та натискання Login користувач бачить помилку Epic sadface: Username and password do not match any user in this service.

**Actual Result:**

Після введення standard_user і не правильного пароля та натискання Login користувач бачить помилку Epic sadface: Username and password do not match any user in this service.

**Result:**

Pass

### TC-LOGIN-03 - Авторизація заблокованого користувача

**Type:** Negative

**Preconditions:**
- відкрита сторінка Login;
- користувач не авторизований.

**Test Data:**
- Username: locked_out_user
- Password: secret_sauce

**Steps:**
1. У поле Username ввести locked_out_user.
2. У поле Password ввести secret_sauce.
3. Натиснути кнопку Login.

**Expected Result:**

Після введення locked_out_user і правильного пароля та натискання Login користувач бачить помилку Epic sadface: Sorry, this user has been locked out.

**Actual Result:**

Після введення locked_out_user і правильного пароля та натискання Login користувач бачить помилку Epic sadface: Sorry, this user has been locked out.

**Result:**

Pass

## Decision Table

| Conditions / Actions                              | R1 | R2 | R3 | R4 | R5 |
|---|---:|---:|---:|---:|---:|
| Username входить до списку допустимих?            | T | T | T | T | ... |
| Password правильний?                              | T | T | F | T | ... |
| Користувач заблокований?                          | F | T | F | T | ... |
| **A1: перехід до Products**                       | X | | | | |
| **A2: повідомлення про блокування**               | | X | | | |
| **A3: повідомлення про неправильні credentials**  | | | ... | ... | ... |

### Покриття Decision Table

- TC-LOGIN-01 → R1
- TC-LOGIN-02 → R3
- TC-LOGIN-03 → R4


## Результати виконання

| Test Case | Type | Result |
|---|---|---|
| TC-LOGIN-01 | Positive | Pass |
| TC-LOGIN-02 | Negative | Pass |
| TC-LOGIN-03 | Negative | Pass |


## Висновок
Навчився розрізняти позитивні та негативні перевірки та застосовувати Decision Table для
систематизації комбінацій умов та фіксувати результати виконання тестів.