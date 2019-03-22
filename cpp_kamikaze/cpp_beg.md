<!-- $theme: gaia -->
<!-- page_number: true -->

C++ для новичков.
=====================
<div align="center"><img src="kamikaze3.jpg" width="35%" >

Путь камикадзе
</div>

---
###### План
<span style="font-size:18px">

* Причины привлекательности С/С++
* Категории изучающих
* Причины сложности С++
	* UB
	* Базовые типы данных и их особенности
	* принцип программного управления и почему он нарушается
	* раздельная компиляция
	* системы сборки
* Внимание! Мины!
	* С++ не первый язык!
	* Принцип постепенного усложнения. 
		* (ограничение по видам приложений, используемым библиотекам и т.п.)
	* Не изучать устаревшее.
	* Не делать того, что не понимаешь.
	* Проверять каждую строчку.
* Выводы

---
# Все хотят изучать С++
* Ну, может быть и не все...
* Но почти каждый день появляются новые и новые люди, желающие изучить С++.
* Иногда они хотят писать быстрые программы
* Иногда они хотят создавать ИИ
* Иногда они хотят на самом деле изучать _**чистый С**_, но не знают об этом, потому что отделить одно от другого сложно для новичка.

### Но что же их привлекает?

---
### Привлекательность С/С++
### С и С++ очень распространены.
<span style="font-size:26px">

* Почти все базовые компоненты и службы всех вычислительных систем написаны на С или С++
	* все операционные системы
	* все СУБД
	* все базовые компоненты WEB
	* все сетевые службы, сетевые устройства

---
### Привлекательность С/С++
* Также на С/С++ написаны
	* множество игр и игровых "движков"
	* библиотеки AI и машинного обучения 
	* библиотеки распознавания текста, речи
	* библиотеки обработки изображения
	* ПО банков и платёжных систем
	* Криптографическое ПО
	* Криптовалюты

---
### С и С++ применяются для создания ПО с высокой производительностью
#### Что же лучше? С или С++?
<span style="font-size:26px">

* С -- довольно слабый, неудобный язык, не обладающий большой мощностью и выразительностью.
* С++ обладает всеми сильными сторонами С, но даёт большее.
* Линус Торвальдс полагает, что С лучше
* Мы уважаем его выбор, но конечно с ним не согласны. <div align="center"><img src="linus.jpg" width="15%" ></div>

---
#### Всё это делает С++ привлекательным языком
<span style="font-size:20px">
(в глазах начинающих)
</span>
<div align="center"><img src="odin.jpg" width="40%">

<p style="color:red">Изучу его - буду богом!</p>
</div>
	
---
###### Кто и зачем изучает С/С++
<span style="font-size:20px">

![Image](study_hard.jpg)

* Студенты ВУЗ, СТО
	- заинтересованные (33% от студентов)
	- в силу наличия в программе (66% от студентов)
* Специалисты
	- расширение знаний и навыков (второй язык)
	- переквалификация (падение спроса на основное направление либо скука)
* Непрофессионалы
	- "а вот я хочу"
	- "чудики"
#### Но какой результат можно ожидать от изучения С++?

---
#### Сложный ли С++ язык?
<span style="font-size:26px">

![Image](cpp_is_easy.jpg)

* Да! Очень сложный!

---
#### Почему С++ такой сложный?
<span style="font-size:20px">
<img src="complexity.jpg" width="30%" height="30%">

##### С++ является одним из самых сложных из существующих языков программирования.
* С++ базируется на С. Сохраняет обратную совместимость.
	```Общяя история двух родственных языков составляет почти 50 лет!```
* С++ - гибридный язык с поддержкой различных парадигм программирования.
* С++ стандартизирован, есть много реализаций-компиляторов, каждый со своими расширениями.
* С++ переносим, но на каждой платформе есть своя специфика. 
* Программа на С/С++ не обязана быть даже целиком валидной с точки зрения языка, но может при этом работать.
---
#### Почему С++ такой сложный?
<img src="matryoshka.jpg" width="30%" height="30%">

##### Внутри С++ содержится как минимум несколько языков по различию в подходах
<span style="font-size:23px">

* Чистый С
* С с классами (С++ до 98го)
* С++ с шаблонами и обобщённым программированием
* С++ с метапрограмами из 2000-ных
* Функциональный С++11
* Современный С++17/20

---
#### Почему С++ такой сложный?
<img src="behemoth.jpg" width="30%" height="30%">

##### Документация на С++ огромна.
<span style="font-size:23px">

|Год|Объём спецификации языка|
|:-:|:-:|
|1990|453 стр|
|1998|776 стр|
|C++11|1353 стр|
|C++14|1370 стр|
|C++17| стр| 

---
#### С чего начинается знакомство с любым языком программирования?

<span style="font-size:27px">

* Принципы функционирования программы (90% Машина Тьюринга)
* Типы данных языка
* Операторы и управляющие конструкции языка
* Системы сборки, поставки и развёртывания

```Работа с каждым языком начинаеся с Hello World!```

---
### Пишем HELLOWORLD на С++

<span style="font-size:23px">

* http://cpp.sh/

```
#include <iostream>
#include <string>

int main()
{
  std::string name;
  std::cout << "What is your name? ";
  getline (std::cin, name);
  std::cout << "Welcome to C++, " << name << "!\n";
}
```

Просто и понятно.
Но хочется большего.

---
### Пишем HELLOWORLD на С++

<span style="font-size:23px">


```
#include <iostream>
#include <string>

int main()
{
  std::string name;
  std::cout << "What is your name? ";
  getline (std::cin, name);
  std::cout << "Welcome to C++, " << name << "!\n"; <<=== Хотим имя БОЛЬШИМИ буквами!
}
```
* Ищем функцию ...
<div align="center">
<img src="toupper.png" width="100%" height="100%">
</div>
*Класс! сейчас сделаем!

---
##### Пишем HELLOWORLD на С++

<span style="font-size:20px">

```
#include <iostream>
#include <string>
#include <cctype>

int main()
{
  std::string name;
  std::cout << "What is your name? ";
  getline (std::cin, name);
  int i = 0;
  std::cout << "Hello, " << char(toupper( name[i++] )) 
                         << char(toupper( name[i++] )) 
                         << char(toupper( name[i++] ))
                         << char(toupper( name[i++] ))
                         << " !"
                         << std::endl;
}
```

---
##### Пишем HELLOWORLD на С++

<span style="font-size:20px">

```
#include <iostream>
#include <string>
#include <cctype>

int main()
{
  std::string name;
  std::cout << "What is your name? ";
  getline (std::cin, name);
  int i = 0;
  std::cout << "Hello, " << char(toupper( name[i++] )) 
                         << char(toupper( name[i++] )) 
                         << char(toupper( name[i++] ))
                         << char(toupper( name[i++] ))
                         << char(toupper( name[i++] ))
                         << char(toupper( name[i++] ))
                         << char(toupper( name[i++] ))
                         << char(toupper( name[i++] ))
                         << char(toupper( name[i++] ))
                         << char(toupper( name[i++] ))
                         << char(toupper( name[i++] ))
                         << char(toupper( name[i++] ))
                         << char(toupper( name[i++] ))
                         << " !"
                         << std::endl;

}
```

---
### Первый прогон!
<div align="center">
<img src="hwrun_1.png" width="100%">
</div>

---
### Первый прогон!
<div align="center">
<img src="hwrun_2.png" width="100%">
</div>

---
### Первый прогон!
<div align="center">
<img src="wtf_pinup.jpg" width="100%">
</div>

---
### Первый прогон!
<div align="center">
<img src="hwrun_3.png" width="100%">
</div>

---
#### Главный принцип работы программы С++
<div align="center">
<img src="UB.jpg" width="70%" height="50%">
</div>

##### Неопределённое поведение.
<span style="font-size:23px">

---
#### Когда это случилось?
##### Не было ничего сложного!
* ни сложных, многофайловых проектов
* ни безумных конструкций препроцессора
* ни сложных математических опрераций
* ни адского темплейтного метапрограммирования
	* ЭТО ВООБЩЕ ДЕТСКИЙ КОД! 
* такое можно было бы писать в школе!

---
### Неопределённое поведение.
<span style="font-size:23px">

#### Что же это такое?
* Что говорит стандарт ANSI/ISO?

``` text
1.3.24 undefined behavior 
behavior for which this International Standard imposes no requirements
```
вроде не страшно...
* Что говорит cpprefecence?
``` text
Renders the entire program meaningless if certain rules of the language are violated.
```
* Так что, вся моя программа неправильная?

---
### Неопределённое поведение.
<span style="font-size:30px">

#### Что же это такое?

_undefined behavior_ - there are **no restrictions on the behavior of the program**. Compilers are **not required to diagnose undefined behavior** (although many simple situations are diagnosed), and the compiled program is **not required to do anything meaningful**. 

---
### Самый главный слайд.
<span style="font-size:38px">

#### UB значит

* Неизвестность
* Помощи не будет !
* Ты один, а вокруг опасность!
<div align="center">
<img src="syl.jpg" width="25%" height="10%">
</div>

---
### Типы данных
<span style="font-size:25px">
Предположим, вы не испупгались UB...

Какие типы данных в распоряжении программиста С/С++?



----
# Подводим итоги ...
<span style="font-size:26px">

  	
---
### Заключение
##### Каковы выводы ?
*

---
Литература
===========================================
* https://ru.cppreference.com
* https://github.com/CppCon/CppCon2017
* https://isocpp.org/blog
* https://github.com/masterziv/meetup.git

---
### Конец

<div align="center">
<img src="stop.png" width="60%" height="1400%">
</div>
