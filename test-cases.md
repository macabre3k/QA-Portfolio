# Страница регистрации

- summary: |
    Проверка регистрации пользователя
  requirement: |
    У сайта должен быть механизм регистрации нового пользователя по email адресу
  prerequisites: |
    Открыть страницу регистрации https://www.garmin.ru/mygarmin/account/?register=yes
  test-data: |
    Nickname = example
    Email = example@gmail.com
    Password = example
    Password Confirmation = example
    Surname = example
    Name = example
    Surname = example

  steps:
    - Ввести данные в поля
    - Нажать кнопку Submit
  expected-result: |
    Происходит редирект на страницу личного кабинета https://www.garmin.ru/personal/


- summary: |
    Проверка повторной регистрации пользователя
  requirement: |
    У сайта должен быть механизм регистрации нового пользователя по email адресу 
  prerequisites: |
    Открыть страницу регистрации https://www.garmin.ru/mygarmin/account/?register=yes
  test-data: |
    Nickname = example
    Email = example@gmail.com
    Password = example
    Password Confirmation = example
    Surname = example
    Name = example
    Surname = example
  steps:
    - Ввести данные в поля
    - Нажать кнопку Submit
  expected-result: |
    Валидация полей ошибку о повторном вводе данных
