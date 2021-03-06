**Цель работы**
Научиться программно работать с файлами и файловой системой, читать, создавать, перемещать и передавать файлы по сети

**Задания для выполнения**
Создать сервер, который предоставляет клиенту базовые возможности файлового менеджера по сети. Клиент после подключения к серверу должен иметь возможности просматривать список файлов и папок в рабочей директории сервера (рабочая директория - это специальная папка, к которой имеет доступ процесс сервера, но она отделена от парки с кодом сервера и от любых системных файлов), создавать и удалять в ней папки, создавать, копировать и переименовывать файлы. Также клиент может передать на сервер название и содержимое файла и сервер должен создать соответствующий файл в текущей директории. Кроме того, клиент может запросить содержимое любого файла и сервер должен передать его в ответ.

Подключение клиента к серверу:
![image](https://user-images.githubusercontent.com/90391164/146352633-05f6325e-6804-46ab-8986-864fc293fab3.png)
![image](https://user-images.githubusercontent.com/90391164/146352643-5f0da996-576e-427e-b955-d35c276ee37f.png)

Создание директории:
![image](https://user-images.githubusercontent.com/90391164/146352823-01539ffe-140a-4711-b15e-be0e58286434.png)
![image](https://user-images.githubusercontent.com/90391164/146352828-4bb52abf-d953-40ba-b91a-743c21f8f4e0.png)

как отображаются действия на сервере в консоли:
![image](https://user-images.githubusercontent.com/90391164/146352913-a3f3a436-c3ed-40fe-a33e-ef3f93d253d3.png)

Создание файла:
создаем текстовый файл в созданной папке командой echo
![image](https://user-images.githubusercontent.com/90391164/146353695-f78e52f0-a6ad-40fd-9b8e-3211af59a93e.png)
Проверим создание:
![image](https://user-images.githubusercontent.com/90391164/146353685-f4b57bcd-e46f-4a6b-93e2-5d514b6fa881.png)

содержимое:
![image](https://user-images.githubusercontent.com/90391164/146354108-b7fe8905-b08d-4754-8ccb-3b78192f5c52.png)

Проверим командой ls содержимое в нашей папке:
![image](https://user-images.githubusercontent.com/90391164/146354258-350bd355-3cde-46a9-9025-af843e3e3885.png)

Отображение всех действий на сервере:
![image](https://user-images.githubusercontent.com/90391164/146354331-c60aee6a-49d1-42ff-8f37-d3687d82076f.png)

командой cat выводим содержимое:
![image](https://user-images.githubusercontent.com/90391164/146354406-0728ee9a-006b-4150-8598-2a4412b88864.png)

перемещение:
![image](https://user-images.githubusercontent.com/80482468/146355874-6ddd358d-b490-486d-9cbc-5fac2b4ef9e2.png)


Удаление файла:
![image](https://user-images.githubusercontent.com/80482468/146357163-9783cc8d-afc1-4e6d-aa91-8bfef3f325b5.png)


Удаление директории:
![image](https://user-images.githubusercontent.com/80482468/146360032-9c17dd99-783e-4e94-92ca-177c67023495.png)

осуществление выхода:
![image](https://user-images.githubusercontent.com/80482468/146360177-272b2f4f-5559-4f86-8b37-c8ea98c12ad2.png)


Дополнительные задания: Ограничьте возможности пользователя рамками одной определенной директории. Внутри нее он может делать все, что хочет: создавать и удалять любые файлы и папки. Нужно проследить, чтобы пользователь не мог совершить никаких действий вне пределов этой директории. Пользователь, в идеале, вообще не должен догадываться, что за пределами этой директории что-то есть.

Проверим:

![image](https://user-images.githubusercontent.com/80482468/146360396-949aced4-6916-4d97-9ea5-6f16d5f9de70.png)

Добавьте логирование всех действий сервера в файл. Можете использовать разные файлы для разных действий, например: подключения, авторизации, операции с файлами.

добавляются в файл log.txt 

![image](https://user-images.githubusercontent.com/80482468/146360520-5e9833a3-bf62-4b6f-9692-db4bef868e50.png)


Добавьте возможность авторизации пользователя на сервере.

Если пользователь уже зарегистрирован и хочет войти под своим именем - ( авторизоваться), он должен ввести цифру 2, затем ввести пароль - ( как на скриншоте ниже - файл клиента)

![image](https://user-images.githubusercontent.com/80482468/146360612-ecdd8e63-4d3e-4971-8583-e8fb59388b9b.png)


данные о пользователях хранятся в файле users.txt
![image](https://user-images.githubusercontent.com/80482468/146360726-a85f6121-fedc-4bdf-83ad-2791b11c3702.png)


Добавьте возможность регистрации новых пользователей на сервере. При регистрации для пользователя создается новая рабочая папка (проще всего для ее имени использовать логин пользователя) и сфера деятельности этого пользователя ограничивается этой папкой.

Если пользователь еще не зарегистрирован в системе - он может это сделать, нажав цифру 1, затем ввести пароль, ( как на скриншоте ниже ) - файл клиента
![image](https://user-images.githubusercontent.com/80482468/146360848-ba668b8d-3fea-400e-a4de-afcfbeb1f9d0.png)

после регистрации данные добавляются в файл users.txt

Реализуйте учётную запись администратора сервера.
![image](https://user-images.githubusercontent.com/80482468/146361058-2b523c1a-2705-4ccd-abef-d63ceeb4baa2.png)
