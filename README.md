> 1. Cкачал Postman
>    https://www.postman.com/downloads/

---

> 2. Изучил документацию
>    https://bump.sh/doc/realworld/operation/operation-createuser

---

> 3. Registration
>    Открыл Postman и создаю новый запрос.

> Установливаю метод запроса на POST.

> URL для регистрации: https://blog-platform.kata.academy/api/users

> Перехожу на вкладку "Body" и выбераю формат raw и тип JSON.

> JSON для регистрации:
> {

       "user": {
         "username": "kukufc",
         "email": "kukufc1234@gmail.com",
         "password": "123456789"
       }
     }

> ответ для зарегистрированного user
> ![ответ для зарегистрированного user](img/registr.png)

> ответ для нового user
> ![ответ для зарегистрированного user](img/registr1.png)

---

> 4.  Логинимся (Authentication)

> Создаю новый запрос в Postman.

> Устанавливаю метод на POST.

> URL для аутентификации: https://blog-platform.kata.academy/api/users/login

> На вкладке "Body" использую тот же формат, и вставляю следующий JSON:
> {

     "user": {
       "email": "kukufc1234@gmail.com",
       "password": "123456789"
     }

}

> Нажмаю "Send". Получаю токен авторизации в ответе, который буду использовать в следующих запросах.
> ![токен авторизации](img/post.png)

---

> 5.  Используя заголовок авторизации получить данные текущего пользователя (Endpoints -> Get Current User)

> Создаю новый запрос.

> Установливаю метод на GET.

> URL: https://blog-platform.kata.academy/api/user

> Перехожу на вкладку "Headers" и добавляю новый заголовок:
> Key: Authorization
> Value: Token eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY3MzBhMWU5Y2UxOGQwMWIwMDJiNTVjNiIsInVzZXJuYW1lIjoia3VrdWZjIiwiZXhwIjoxNzM3NTQ3OTIyLCJpYXQiOjE3MzIzNjM5MjJ9.X_VqFzywiY-jpgtrRFtku08ivgLz_yOWuGzkh7epJEk
>
> > (важно не забыть написать "Token ..." )

> Нажмаю "Send". Получаю данные пользователя в формате JSON.
> ![данные пользователя](img/get.png)

---
