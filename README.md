<h1 align="center"> Taxi-Service </h1> <br>

<p align="center">
  Програма дозволяює переглядати, налаштовувати і змінювати списки 
            таксопарку лише зареєстрованим користувачам-водіям.
</p>

```
примітка: користувач та водій і є юзей. Завдяки цому водії можуть користуватися програмою
```


## Table of Contents

- [Більш детальний опис функціональності](#functionality)
- [Структура проекту](#project-structure)
- [Використані технології](#technologies-used)
- [Інструкції по запуску проекту](#instructions)
---

## functionality

#### Login :
Программа taxi-service вітає нас на головній сторінці логін. Де відбувається реєстрація і вхід до таблиці сервісу.
 - [переглянути структуру сторінки логін](#login-page)
![](READMEimages/login.png)

#### _Add driver_ :
У випадку коли юзер не зареестрований ми можемо додати його завдяки кнопці 'Add driver' що дозволяє створити нового водія-користувача та занести його до бази даних таксопарку.
 - [переглянути структуру сторінки 'Add driver'](#add-driver)
![](READMEimages/add-driver.png)

#### _Taxi service_ :
Якщо пароль і логін існують в нашій базі даних то ми потрапляємо на сторінку 'Taxi service' це меню складається з 8 пунктів.
Сім пунктів відповідають за посилання на меню та таблиці і один це кнопка 'current driver' яка демонструє всі машини користувача,що залогінівся і знаходится в меню 'Taxi service'
![](READMEimages/taxi-service.png)



```
1.Посилання 'Display All Drivers' переность на 'All Drivers', що містить всіх водіїв що значиться у таксопарку.
```
 - [переглянути структуру сторінки 'All Drivers'](#all-drivers)
![](READMEimages/all-Drivers.png)



```
2.Посилання 'Display All Cars' переность на 'All cars', що містить всі машини що значиться в таксопарку
```
 - [переглянути структуру сторінки 'All Cars'](#all-drivers)
![](READMEimages/all-cars.png)



```
3.Посилання 'Display All Manufacturers' переность на таблицю 'All manufacturers:', яка містить всіх виробників що значиться в таксопарку
```
 - [переглянути структуру сторінки 'All manufacturers'](#all-manufacturers)
![](READMEimages/all-manufacturers.png)



```
4.Посилання 'Create new Driver' переность на сторінку з меню 'Add driver', дозволяє створити нового водія-користувача та занести його до бази даних таксопарку.
```
 - [переглянути структуру сторінки 'Add driver'](#add-driver)
![](READMEimages/add-driver.png)


```
5.Посилання 'Create new Car' переность на сторінку з меню 'Add car', створити нову машину і занести її до нашої бази
```
 - [переглянути структуру сторінки 'Add car'](#add-car)
![](READMEimages/add-car.png)


```
6.Посилання 'Create new Manufacturer' переность на сторінку з меню 'Add manufacturer', дозволяє створити нового виробника машин і занести його до нашої бази
```
 - [переглянути структуру сторінки 'Add car'](#add-manufacturer)
![](READMEimages/add-manufacturer.png)


```
7.Посилання 'Add Driver to Car' переность на сторінку з меню 'Add driver to car', дозволяє закріпити водія за автомобілем
```
 - [переглянути структуру сторінки 'Add driver to car'](#add-driver-to-car)
![](READMEimages/add-driver-to-car.png)


```
8.кнопка 'current driver' ця кнопка йде останньою у меню 'Taxi service' та демонструє всі машини користувача, що залогінівся і знаходится в цому меню. При натискані відкриває таблицю 'All cars' але фільтр виводить лиге автомобілі залогіненого користувача
```
 - [переглянути структуру сторінки 'Add driver to car'](#all-cars-current)
![](READMEimages/all-cars-current.png)

---

## project-structure

##### login-page 

1. 'Please enter your login:' - вести логін водія
2. 'Please enter your password:' - вести пароль водія
3. кнопка 'login' - дозволяє залогінитись і прейти до сторінки 'Taxi service' де ми і можемо керувати нашим таксопарком.

		примітка: Якщо юзер заерестрований то ми попадемо до меню 'Taxi service',
		якщо ні то випливе назва "Username or password was incorrect" що вказу на те що такого користувача нема в нашій базі
		
4. кнопка 'add new driver' - дозволяє створити нового водія-користувача після натискання нас перенесе на сторінку 'Add driver' де ми і рееструємо нового водія-користувача.

##### add-driver

1. В поле 'Name' - вести імя водія-користувача
2. В поле 'License number' - вести особистий ідетифікатор водія
3. В поле 'login' - вести логін водія
4. В поле 'password' - вести пароль водія
5. потім потрібно натиснути кнопку
	"Add" яка іде одразу після всіх заповнених полів.
	Новий юзер збережеться до нашої бази 

##### all-drivers

1. ID ~ Особистий ідетифікатор водія
2. Name ~ Імя водія
3. License number ~ Особистий ліцензійний номер водія 
4. login ~ логін водія
5. password ~ пароль водія
6. delete ~ дозволяє видилити водія з таксі сервісу

##### all-manufacturers
1. ID ~ Особистий ідетифікатор виробника автомобіля
2. Name ~ Назва виробника автомобіля
3. Country ~ Вказує на країну походження виробника
4. Delete ~ Дозволяє видилити виробника з таксі сервісу

##### add-car
1. В поле 'Model' - вести модель автомобіля
2. В поле 'Manufacturer ID' - ввести ідентифікаційний номер виробника який знаходится у таблиці 'All manufacturers'
```
'All manufacturers' в колонці 'ID'. Це потібно щоб програма змогла знайти виробника нашої машини
``` 
3. потім потрібно натиснути кнопку "Add" яка іде одразу після всіх заповнених полів. Новий автомобіль буде збережений до нашої бази 

##### add-manufacturer
1. В поле 'Name' - вести назву заводу автомобілей
2. В поле 'Country' - ввести країну виробника
3. потім потрібно натиснути кнопку "Add" яка іде одразу після всіх заповнених полів. Новий виробник буде збережений нашої бази 

##### add-driver-to-car
1. В поле 'Car ID' - вести ідетифікатор машини
```
ідетифікатор машини знаходеться в таблиці 'All cars' в колонці 'ID'
```
2. В поле 'Driver ID' - вести ідетифікатор водія
```
ідетифікатор водія знаходеться в таблиці 'All Drivers' на колонці 'ID'
```
3. потім потрібно натиснути кнопку "Add" яка іде одразу після всіх заповнених полів. Водій що був обран по id буде доданий до машини що була обрана по id

##### all-cars-current
1. ID ~ Особистий ідетифікатор автомобіля
2. Manufacturer name ~ Назва виробника автомобіля
3. Manufacturer country ~ Вказує на країну походження виробника
4. Drivers ~ ця колонка демонструє водіїв записаних за цим автомобілем
```
 колонка 'Drivers' містить 3 значення з таблиці 
 'All Drivers', a came
 	  ID, Name, License number
```
6. delete ~ дозволяє видилити машину з таксі сервісу
---
## technologies-used
##### у цьому проекті були використані такі інструменти як:

 	MySQL Workbench
 	apache-tomcat-9.0.75

---
## instructions
1. Підключитися до SQL за допомогою консолі:
```
~ % /usr/local/mysql/bin/mysql -u root -p
Enter password: (пароль на SQL)
```
2. Встановити MySQL Workbench та створити connection
і вессти пароль mysql що ми створили у консолі
![](READMEimages/MySQL-workbench.png)

3. Скопіювати sql запит з проэкту та вставити у Workbench
![](READMEimages/sql.png)

4. Завантажити apache-tomcat-9.0.75 на свій компютер і
запустити його в intellij idea. Для цого переходимо в Edit Configurations... і обераємо локальний tomCat
![](READMEimages/tomCat.png) 
Потім натискаємо Configure і додаємо наш шлях до дерикторії з tomCat
![](READMEimages/tomCat2.png) 
після натискаємо fix і обераємо (web-practice:war exploded) і змінюємо адресу з "/taxi_service_war_exploded" на "/"
---





