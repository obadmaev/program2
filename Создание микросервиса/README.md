**Создание микросервиса**
**Цель работы**
Познакомиться с механизмом работы современных веб-приложений и микросервисной архитектуры в процессе выполнения творческого задания.

**Задания для выполнения**
- На основе предложенного шаблона реализуйте сервис, реализующий регистрацию пользователей. Сервис должен поддерживать REST API и коллекцию /user/, хранящую данные о логинах и паролях пользователей, зарегистрированных в системе. Сервис должен принимать и отдавать информацию в формате JSON. Сервис должен хранить следующую информацию про каждого пользователя: логин, хеш пароля (лучше с солью), дату регистрации.

- Настройте веб-сервер по Вашему выбору (Apache2 или nginx) таким образом, чтобы он поддерживал соединение по протоколу HTTPS. Для этого сгенирируйте самоподписанный сертификат SSL.

- Модифицируйте код вашего сервиса таким образом, чтобы он поддерживал защищенное соединение.






1.
Для тестирования используем модуль requests, который, собственно, и позволяет производить запросы.
При хэшировании в поле ввода password добавляется соль(модификатор входа хэш-функции) для более удобного получения её в будущем. Также благодаря ней сервис позволяет создавать пользователей с одинаковыми паролями и разными именами. При попытке создать пользователя с уже существующем именем сервер выдает сообщение об ошибке, также это происходит и при попытке получить данные по несущетвующему пользователю.
![image](https://user-images.githubusercontent.com/80482468/146441172-a714d202-a240-4547-b2b2-d167fc46f105.png)

![image](https://user-images.githubusercontent.com/80482468/146441183-e4ac58ef-838d-41a9-bb9d-417488c3c5cf.png)

![image](https://user-images.githubusercontent.com/80482468/146441188-ed26755c-396f-4897-8b04-651511904206.png)




2.Настройте веб-сервер по Вашему выбору (Apache2 или nginx) таким образом, чтобы он поддерживал соединение по протоколу HTTPS. Для этого сгенирируйте самоподписанный сертификат SSL.

![image](https://user-images.githubusercontent.com/80482468/146452958-4ff43305-6936-4148-910c-566dedec2baa.png)

![image](https://user-images.githubusercontent.com/80482468/146452979-6703f20e-876c-49df-be0f-65febdf05360.png)
![image](https://user-images.githubusercontent.com/80482468/146453000-081da313-942f-420f-b086-01fc1936c0bb.png)

![image](https://user-images.githubusercontent.com/80482468/146446818-eac026a8-bfc9-4366-a26b-a427ba26d081.png)



3.Модифицируйте код вашего сервиса таким образом, чтобы он поддерживал защищенное соединение.

![image](https://user-images.githubusercontent.com/80482468/146453026-bbfa560c-5578-4b4e-9fe9-ba5662cbe047.png)
![image](https://user-images.githubusercontent.com/80482468/146453056-80228637-7ea2-4309-bcfb-0c9af47140c0.png)
![image](https://user-images.githubusercontent.com/80482468/146446964-69bf4feb-a63c-4085-80f3-2bd28248e2b0.png)




