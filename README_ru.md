* [Университет Низкоуровневого Программирования](#Университет-Низкоуровневого-Программирования)
  * [Что это такое?](#What-is-it)
  * [Что значит "низкоуровневый"?](#what-Is-the-Low-Level)
  *  [Теория](#Theory)
  *  [Языки](#Languages)
     * [Ассемблер](#Assembly)
     * [Язык C](#C-language)
     * [Rust](#Rust-language)
  * [Приложения](#Applications)
    * [Аппаратное обеспечение && Прошивка](#Hardware-Firmware)
    * [Ядро Linux и драйвера устройств](#Linux-kernel-and-device-driver)
      * [Ссылки](#References)
    * [Прочие приложения](#Other-applications)
  * [Будущее низкоуровневого программирования](#Future-of-low-level-programming)
  * [Как начать?](#How-to-start)
* [Перевод](#Translation)
* [Кто я такой?](#who-am-i)

# Университет Низкоуровневого Программирования

## <a name="What-is-it"></a>Что это такое?

Вдохновляясь [google-interview-university](https://github.com/jwasham/coding-interview-university), мне бы хотелось поделиться опытом и показать путь к становлению программистом низкоуровневого программного обеспечения, потому что я обнаружил, что эти навыки стали не так распространены, как раньше. 
Кроме того, многие студенты и новички спрашивают меня, как им стать разработчиками низкоуровневого программного обеспечения и инженерами ядра Linux в частности.

Очевидно, что на одной странице невозможно уместить все ссылки/книги/курсы. 
Например, на этой странице представлен Arduino, но нет подробной информации об Arduino и встроенных системах. 
Вам следует продолжать путь самостоятельно. 
Так что ваш следующий шаг, вероятно, — это изучить информацию об Arduino в вашей любимой поисковой системе, купить комплект и сделать что-то для себя, а не просто собирать ссылки или бесплатные книги. 
Помните, что эта страница — всего лишь дорожная карта для новичков.

Примечание [переводчиков](https://github.com/LabunskyA):
не для всех ссылок и книг существует русскоязычный аналог или перевод. 
Тех, что нашел, должно быть достаточно для начала пути, но, в любом случае, английский язык является необходимым навыком для успешного развития своих навыков в данной сфере. 
Поэтому к оригинальным советам добавлю от себя: **учите английский**.

## <a name="What-Is-the-Low-Level"></a>Что значит "низкоуровневый"?

Я отношу низкоуровневое программирование к программированию очень близкому к устройству, для него используются языки низкоуровневого программирования, такие как C или ассемблер. 
В этом его отличие от программирования более высокого уровня, ориентированного на приложения пользовательского пространства, с использованием языков высокого уровня (например, Python, Java).
* [Wikipedia: Язык программирования низкого уровня](https://en.wikipedia.org/wiki/Low-level_programming_language), [на русском](https://ru.wikipedia.org/wiki/Низкоуровневый_язык_программирования)

Да, системное программирование очень близко к низкоуровневому программированию. 
На этой странице также затрагиваются темы проектирование аппаратных средств и разработки прошивок, которые не входят в понятие системного программирования.
* [Wikipedia: Системное программирование](https://en.wikipedia.org/wiki/System_programming), [на русском](https://ru.wikipedia.org/wiki/Системное_программное_обеспечение)

Наконец, на этой странице представлены самые разные темы: от аппаратных компонентов до ядра Linux. Это огромный диапазон слоёв. 
Одностраничный документ никогда не сможет охватить детали всех слоев, поэтому его основная задача — быть отправной точкой в мир низкоуровневого программирования.

##  <a name="Theory"></a>Теория

Низкоуровневое программирование основывается на двух теориях:
* Архитектура Компьютеров
* Операционные Системы

Я думаю, что лучший способ изучить теорию - пройти соответствующий курс. Чтение книг само по себе не плохо, но отнимает слишком много времени и сил. 
При желании, можно найти много хороших курсов в онлайн университетах, в частности, на coursera.org и edx.org.
Но теория - это лишь теория. Не думаю, что необходимо закончить курс на отлично, чтобы разобраться в теме.
С опытом вы будете становиться все лучше и лучше.

Позволь мне представить несколько книг, которые я прочёл. Они широко используются в качестве учебников в университетах.
Если в вашем университете не было занятий с этими книгами, стоит потратить некоторое время на их чтение. 
* Архитектура Компьютеров
  * Computer Architecture, Fifth Edition: A Quantitative Approach 
  * [Компьютерная Архитектура. Количественный подход. Издание 5-е](http://www.technosphera.ru/files/book_pdf/0/book_348_882.pdf)
  * Computer Systems: A Programmer's Perspective 
  * [Компьютерные системы: архитектура и программирование](https://www.google.com/search?q=%D0%9A%D0%BE%D0%BC%D0%BF%D1%8C%D1%8E%D1%82%D0%B5%D1%80%D0%BD%D1%8B%D0%B5+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B%3A+%D0%B0%D1%80%D1%85%D0%B8%D1%82%D0%B5%D0%BA%D1%82%D1%83%D1%80%D0%B0+%D0%B8+%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5) 
  * Computer Organization and Design, Fourth Edition: The Hardware/Software Interface 
  * [Архитектура компьютера и проектирование компьютерных систем](https://www.google.com/search?q=%D0%9F%D0%B0%D1%82%D1%82%D0%B5%D1%80%D1%81%D0%BE%D0%BD%2C+%D0%A5%D0%B5%D0%BD%D0%BD%D0%B5%D1%81%D1%81%D0%B8%3A+%D0%90%D1%80%D1%85%D0%B8%D1%82%D0%B5%D0%BA%D1%82%D1%83%D1%80%D0%B0+%D0%BA%D0%BE%D0%BC%D0%BF%D1%8C%D1%8E%D1%82%D0%B5%D1%80%D0%B0+%D0%B8+%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5+%D0%BA%D0%BE%D0%BC%D0%BF%D1%8C%D1%8E%D1%82%D0%B5%D1%80%D0%BD%D1%8B%D1%85+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC.+%D0%9A%D0%BB%D0%B0%D1%81%D1%81%D0%B8%D0%BA%D0%B0+Computers+Science)
* Операционные системы
  * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design
  * The Design of the UNIX Operating System 
  * [Архитектура операционной системы Unix](http://rsusu1.rnd.runnet.ru/unix/bach/chap02.html)
  * Operating Systems: Internals and Design Principles by William Stallings 
  * [Операционные системы](https://www.google.com/search?q=%D0%9E%D0%BF%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D1%8B%D0%B5+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B+%7C+%D0%A1%D1%82%D0%BE%D0%BB%D0%BB%D0%B8%D0%BD%D0%B3%D1%81+%D0%92%D0%B8%D0%BB%D1%8C%D1%8F%D0%BC)
* Рекомендуемые курсы
   * [CS401: Operating Systems](https://learn.saylor.org/course/CS401)
* Общие навыки программирования
  * [Структура и интерпретация компьютерных программ](https://en.wikipedia.org/wiki/Structure_and_Interpretation_of_Computer_Programs), [на русском](https://ru.wikipedia.org/wiki/%D0%A1%D1%82%D1%80%D1%83%D0%BA%D1%82%D1%83%D1%80%D0%B0_%D0%B8_%D0%B8%D0%BD%D1%82%D0%B5%D1%80%D0%BF%D1%80%D0%B5%D1%82%D0%B0%D1%86%D0%B8%D1%8F_%D0%BA%D0%BE%D0%BC%D0%BF%D1%8C%D1%8E%D1%82%D0%B5%D1%80%D0%BD%D1%8B%D1%85_%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC)
    * Речь идет о том, как стать хорошим программистом. Вам нужна не только теория, но и техника, потому что программирование — это своего рода ремесло.
    * Если вы изучите Lisp/Scheme, вы сможете быстро выучить любой другой язык.
    * [Я решил около 80% упражнений. Стоит попробовать каждое упражнение](https://github.com/gurugio/sicp_exercise)
* Системный дизайн
  * Соберите свой собственный комплект микропроцессора 8086
    * Если вы не создадите свою аппаратную плату, вы не поймете, что такое устройство с отображением физической памяти.
    * Современные точки доступа включают в себя очень много IP-адресов. Таким образом, у вас нет возможности понять, как связаны ядро процессора и периферийные устройства.
    * Когда вы создаете свой собственный комплект 8086, у вас есть возможность найти каждое периферийное устройство в физической памяти. И вы можете своими глазами увидеть работу основных аппаратных компонентов (BUS, IRQ, Clock, Power и т.д.).
    * Я собрал комплект 8086 в своем университете. Это был один из самых ценных курсов, которые я когда-либо посещал. Попробуйте собрать свой собственный комплект аппаратного обеспечения. Было бы лучше, если бы аппаратное обеспечение было старше и проще, потому что вам придется больше делать для себя.
    * Найдите в своей любимой поисковой системе «комплект 8086». Вы сможете найти несколько веб-сайтов, на которых можно купить аппаратную схему, детали и ознакомиться с руководствами.


Список хороших книг бесконечен. Не хочу сказать, что нужно перемолоть множество книг: достаточно и одной, но прочитанной внимательно. 
Старайтесь подкреплять все свои новые знания практикой. **Порой "Одна практическая реализация лучше, знания сотни теорий"**

##  <a name="Languages"></a>Языки

### <a name="Assembly"></a>Ассемблер

Выберите одну из платформ, х68 или ARM, необходимости в доскональном изучении обеих нет смысла. Даже не столь важно знание самой реализации языка ассемблера. 
Гораздо важнее глубокое понимание работы процессора и компьютера в целом. 
Знание последних новинок реализации языка ассемблера не так важно, так что для начала лучше выбрать 8086 или Cortex-M, но также подойдёт и любой процессор имеющийся у вас.

* [Программирование на ассемблере 8086 с помощью emu8086](https://github.com/gurugio/book_assembly_8086)
  * базовые концепты процессора и архитектуры компьютера
  * базовые концепты языка программирования C
* [Программирование на 64-битном ассемблере (перевод на англ. в процессе)](https://github.com/gurugio/book_assembly_64bit)
  * базовые концепты современного процессора и архитектуры компьютера
  * базовые концепты дезассемблирования и отладки кода на C
  * _нужна помощь в переводе на английский_
* [ARM Architecture Reference Manual, 2nd Edition](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-9780201737196)
  * Полная справка по программированию на ARM
* [Паттерсон, Хеннесси: Архитектура компьютера и проектирование компьютерных систем](https://www.labirint.ru/books/317754/)
  * [MIPS Edition](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
  * [ARM Edition](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
  * [RISC-V Edition](https://www.amazon.com/Computer-Organization-Design-RISC-V-Architecture/dp/0128122757),  [русскоязычный аналог](https://is.ifmo.ru/books/2016/digital-design-and-computer-architecture-russian-translation_July16_2016.pdf)
  * Академические книги, объясняющие работу каждого компонента компьютера с самых основ.
  * Подробно рассматриваются различные концепции, составляющие компьютерную архитектуру.
  * Они не ориентированы на читателя, желающего стать специалистом определенной реализации языка ассемблера.
  * Издания для MIPS и ARM охватывают одни и те же темы, но рассматривают разные архитектуры.
  * Оба издания содержат примеры из мира x86

### <a name="C-language"></a>Язык C

Тут коротких путей нет. Просто читай всю книгу и решай все упражнения.

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN) 
* [Брайан У. Керниган, Деннис М. Ритчи, Язык программирования C, 2-е издание](https://www.ozon.ru/context/detail/id/2480925/)
* [Modern C](http://icube-icps.unistra.fr/img_auth.php/d/db/ModernC.pdf)
  * Для нового стандарта C
* [Is Parallel Programming Hard, And, If So, What Can You Do About It?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
  * базовая реализация синхронизации в C
  * Необходим для крупномасштабного программирования на C (особенно, для программирования на уровне ядра)
* [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/)
  * Если ты закончил читать одну или две книги по C, то ты ДОЛЖЕН начать делать что-нибудь.
  * Выбери что угодно по нраву.
  * Сначала, сделай что-нибудь свое, после чего сравни с чужим исходным кодом. Очень важно проводить подобные сравнения. Улучшить свои навыки можно только при чтении чужого кода, обучаясь использованию лучших методов. Книги мертвы, код же живет.
* [Проекты на C и других языках](https://github.com/danistefanovic/build-your-own-x)
  * Найди больше интересных проектов
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
  * Справочник по оптимизации с использованием C и капли ассемблера x86
  * Начиная с 8088 до сегодняшнего дня
  * Особый фокус на низкоуровневых оптимизациях графики
* [Framework and plugin design in C (Korean)](https://github.com/gurugio/book_cprogramming)
  * Как разработать фреймворк и плагин на C для крупномасштабного ПО
  * Планируется перевод на английский

Если хочешь стать экспертном в программировании на C, посети https://leetcode.com/. Удачи!

### <a name="Rust-language"></a>Rust

I am sure that the next language for the systems programming would be Rust.
I will make a list what I did to learn Rust.

[Linus Torvalds said "Unless something odd happens, it [Rust] will make it into 6.1."](https://www.zdnet.com/article/linus-torvalds-rust-will-go-into-linux-6-1/)

* [The Rust Programming Language](https://doc.rust-lang.org/book/)
  * Great introduction, but lack of examples and exercises.
* [Rust by Example](https://doc.rust-lang.org/rust-by-example/)
  * While reading "The Rust Programming Language", you can find examples and exercises here.
  * But there are not many exercises you can do something for yourself. Only some examples includes "do-this" exercises and they are very simple.
* [Programming Rust, 2nd](https://www.oreilly.com/library/view/programming-rust-2nd/9781492052586/)
  * Deeper introduction, but still lack of examples and exercises.
* [Exercism](https://exercism.org/tracks/rust)
  * Good exercises to practice indivisual features of RUST.
  * I am not sure Mentors are working actively but it would be enough to compare your solution with others.
    * After submitting your solution, you can see other's solutions with "Community solutions" tab (since Exercism V3).
    * Many easy level exercises are for functional feature such as map/filter/any and etc.
* [Easy rust](https://dhghomon.github.io/easy_rust/)
  * A book written in easy English.
  * Youtube materials provided: https://www.youtube.com/playlist?list=PLfllocyHVgsRwLkTAhG0E-2QxCf-ozBkk
* [Let's get rusty](https://www.youtube.com/c/LetsGetRusty)
  * There are many Youtubers uploading Rust course but I enjoyed this course most.
  * He has been uploading the latest news for Rust. It's worth subscribing.
* [Rust for Linux](https://github.com/Rust-for-Linux)
  * See the example sources and check how Rust will get into the Linux kernel


## <a name="Applications"></a>Приложения

### <a name="Hardware-Firmware"></a>Аппаратное обеспечение && Прошивка

Если хочешь стать системным инженером встраиваемых систем, то лучше начать с простых kit'ов для разработки, нежели с последнего чипсета ARM.

* [Arduino Start Kit](https://www.arduino.cc/)
  * Существует множество серий Arduino, но "Arduino Start Kit" имеет наиболее простой процессор (Atmega328P) и книгу-гайд.
  * Atmega328P имеет 8-битное ядро, с которого хорошо начинать в сфере проектирования цифровых схем и разработки прошивок.
  * Тебе не требуется знать, как создавать схематики и макеты, а так же собирать чипы.
  * Но нужно знать, как читать схематики и понимать, как чипы соединены между собой.
  * Разработчик прошивок должен уметь читать схематики и понимать, как передать данные на целевое устройство.
  * Следуй гайду!
* [8086 manual](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * Если ты не знаком с архитектурой x86, то 8086 также является хорошим гайдом архитектуры процессора и ассембрела 80x86
* [80386 manual](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * Лучший гайд защищенног режима и механизма подкачки страниц процессора 80x86
  * Веб-версия: https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm

К этому моменту, можно приступать к последним процессорам архитектур ARM и x86.
* https://www.raspberrypi.org/
* https://beagleboard.org/
* https://www.arduino.cc/en/ArduinoCertified/IntelEdison

Для примера, плата Raspberry Pi имеет процессор Cortex-A53, поддерживающий 64-битный набор инструкций.
Это позволяет получить опыт в работе с современной процессорной архитектуры с помощью rPi.
Да, его можно купить... но... что ты собираешься с ним делать?
Если нет целевого проекта, скорее всего ты просто положишь плату в дальний ящик и забудешь о ней как и обо всех других, купленных до этого.

Поэтому, я рекомендую следующий проект.
* [Создание своего собственного ядра](http://wiki.osdev.org/Getting_Started)
  * Хорошие ссылки: https://www.reddit.com/r/osdev/
* [Учимся разработке операционных систем используя Linux и Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
  * (Описание проекта) Этот репозиторий содержит пошаговый гайд, учащий создавать простое ядро операционной системы с нуля...(пропуск)...Каждый урок создан таким образом, что сначала объясняет, как некоторые фичи ядра реализованы в RPI OS, и лишь потом пытается продемонстрировать работу подобного функционала в ядре Linux.

Я сделал [игрушечное ядро](https://github.com/gurugio/caos), поддерживающее 64-битный "длинный" режим, подкачку страниц и очень простое переключение контекста. создания ядра является хорошим способом понять архитектуру современного компьютера и управление "железом".

Вообще говоря, у тебя уже есть доступ к последнему процессору и последним аппаратным устройствам.
Твой ноутбук! Твой ПК! Ты уже имеешь все необходимое для старта!
Не нужно ничего покупать.
QEMU может эмулировать последние процессоры ARM и x86.
То есть, все необходимое на руках.
Существует множество игрушечных ядер и документации для справки.
Просто установи QEMU эмулятор и создай микро-ядро, которое способно загрузиться, включить подкачку и вывести текстовые сообщения. 

Другие игрушечные ядра:
* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-kernel-and-device-driver"></a>Ядро Linux и драйвера устройств

Не нужно создавать свою полноценную операционную систему.
Присоединйяся к сообществу Linux и участвуй в разработке.

Some resources for Linux kernel and device driver development from beginner to advanced.
* Books: Read the following in order
  * [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
    * The basic concepts of Unix are applied into all operating systems.
    * This book is a very good place to learn the core concepts of operating systems.
  * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * Make all examples for yourself
  * [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
    * Understand the design of the Linux Kernel
  * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
    * Read this book and the kernel source v2.6 at the same time
    * Never start with the latest version, v2.6 is enough!
    * Use qemu and gdb to run the kernel source line by line
      * http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu
      * https://github.com/gurugio/linuxdeveloptip/blob/master/qemu-gdb-kdump.md
    * Use busybox to make the simplest filesystem that takes only one second to boot
      * https://github.com/gurugio/linuxdeveloptip/blob/master/minikernelwithbusybox.md
* Other resources: Free resources I recommend
  * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * Practical guide and excellent exercises making Linux device drivers with essential kernel APIs
    * I think this document introduces almost all essential kernel APIs.
  * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
    * _Sadly, this challenge does not accept new challengers because there is no challenge anymore._ The maintainer said he/she is planning a new format. I hope it comes back ASAP.
      * But you can find the questions of the challenge with Google. Some people already uploaded what they did. Find the questions and try to solve them on your own, and compare your solution with others.
    * This is like an awesome private teacher who guides you on what to do.
    * If you don't know what to do, just start this.
  *  [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
    * This project is not completed yet.
    * I always think making a kernel similar to the Linux kernel is the best way to understand the Linux kernel.
  * [Block layer and device driver](https://github.com/gurugio/book_linuxkernel_blockdrv)
    * start from a simple block device driver example (Ramdisk) with multi-queue mode
    * go forward to block layer
    * I completed translation into English. Please send me your feedback.
  * [md driver of Linux kernel(Korean)](https://github.com/gurugio/book_linuxkernel_md)
    * how mdadm tool works and how it calls md driver
    * how md driver works
  * [A Heavily Commemted Linux Kernel Source Code](http://www.oldlinux.org/)
    * Heavy comments for the ancient Linux v0.12.
    * It would be good to start with old and simple OS.
    * Unix version: [Lions' Commentary on UNIX 6th Edition, with Source Code](https://en.wikipedia.org/wiki/Lions%27_Commentary_on_UNIX_6th_Edition,_with_Source_Code)

#### <a name="References"></a>Ссылки

Посмотри здесь, если понадобится что-то еще

* [Free-electrons homepage](http://free-electrons.com/docs/)
  * множество презентаций, представляющих хорошие темы, особенно Linux на ARM
* [Julia Evans's posting: You can be a kernel hacker!](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * гид для входа в программирование уровня ядра

### <a name="Other-applications"></a>Прочие приложения

Да, ты можешь быть и не заинтересован в линуксе и прошивках. Если так, то можно найти и другие сферы:
* Системное программирование и драйвера устройств под Windows
* Безопасность
* Реверс инженеринг

У меня нет каких-либо знаний в данных сферах. Поэтому прошу отправить мне любую информацию о них для новичков.

**Ядра и драйверы - еще не все низкоуровневое программирование.** Одним из наиболее важных приложений низкоуровневого программирования являются распределенные файловые системы и хранилища. Подробное их описание находится на пределами фокуса этого документа, но существует отлличный курс, в котором можно попробовать себя в данной сфере. 
* Курс: https://pdos.csail.mit.edu/archive/6.824-2012/
* Исходный код для работы с ним: https://github.com/srned/yfs

## <a name="Future-of-low-level-programming"></a> Будущее низкоуровневого программирования

Мне неизвестно будущее, но я посматриваю на RUST.
* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

Если бы у меня была свободная неделя в одиночестве, я бы его выучил.
Просто потому, что RUST - самый новый язык программирования, на котором возможна разработка драйверов устройств под Linux.
* https://github.com/tsgates/rust.ko

IoT теперь уже является трендом, поэтому стоит посмотреть на ОС для него.
ARM, Samsung и некоторые другие компании имеют свои собственные ОС реального времени, но, к сожалению, многие из них имеют закрытый исходный код.
Но Linux Foundation также имеет свое решение: Zephyr
* https://www.zephyrproject.org/

Обычные облачные сервера имеют множество слоев; в частности, хостовую ОС, драйвер kvm, процесс qemu, гостевая ОС и сервисное приложение. Контейнер был создан, чтобы предоставить легку. виртуализацию. В ближайшем будущем, новый концепт ОС, так называемый "библиотечная ОС" или Unikernel, может заменить типичный стэк SW для виртуализации.
* http://unikernel.org/

Big data и облачные вычисления требуют хранения все больших и больших объемов данных. Некоторые диски, напрямую подключенные к серверам, не могут удовлетворить требующуюся емкость, стабильность и производительность. Поэтому были проведены исследования для создания больших систем хранения данных с помощью множества машин, соединенных высокоскоростной сетью. Поначалу они были сфокусированы на создании одного большого тома-хранилища. Но теперь предлагаю множества томов, выделенных для множества виртуальных машин.
* https://en.wikipedia.org/wiki/Software-defined_storage
* https://en.wikipedia.org/wiki/Clustered_file_system
* https://en.wikipedia.org/wiki/Ceph_(software)

## <a name="How-to-start"></a>How to start?

Я получил электронное письмо с вопросом, как начать. На этой странице много информации о книгах, курсах и проектах. 
Моя ошибка, что я забыл написать с чего начать. 
К сожалению простого пути нет [в оригинале "King's Road to King's Landing"](https://gameofthrones.fandom.com/wiki/King%27s_Landing). 
Можете последовать моему пути или открыть новый. Далее предложен мой путь. Если вы уже изучали один из разделов, вы можете пропустить его. 
ДИСКЛЕЙМЕР, это всего лишь один из вариантов и вы можете последовать ему если не знаете с чего начать.

* Для начала познакомьтесь с теорией операционных систем: к примеру [Морис Дж. Бах. Архитектура операционной системы Unix](http://rsusu1.rnd.runnet.ru/unix/bach/chap02.html)
* Изучите язык ассемблера и языки C
  * [Программирование на языке ассемблера NASM для ОС UNIX](https://mega.nz/file/w7lWxTwT#MlO8PELceTS8ZG2xylvjHD1-XxMnQRAn_xQupAAcZEw), или [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
    * Будет достаточно, если вы понимаете концепцию программирования на ассемблере, количество практики зависит от вашего желания. 
  * [Язык программирования Си 2 Издание](https://www.google.com/search?q=%D0%AF%D0%B7%D1%8B%D0%BA+%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F+%D0%A1%D0%B8+%28%D0%BA%D0%BD%D0%B8%D0%B3%D0%B0%29&si=ALGXSla9etGlV4pbaO8olaorTsiB-x9zbiuViqVo7rMUgudilzgfiF9EeEB7leFM01GnttW26HHw-JZNw_soWCH6tE_eTC5dOka2pmCwOHTvDSHPI1ekrc0orrrlqjNi495dLo5WI4LdQgxS7CcHEwc9PNmOl8f87HipRXu7S-8ii05pxkrVwt4%3D)
    * Постарайтесь выложиться на полную решая задания предложенные в книге.
  * [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* Попробуйте применить C на практике
  * [Уроки по проектам C](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/): Посмотри предложенные идеи или реализуй свою.
  * [leetcode.com](https://leetcode.com/): Если у вас не получается найти интересную идею для проекта, потренируйтесь в реализации алгоритмов и структур данных.
* Сделать аппаратный проект
  * Выберите себе Raspberrypi или Arduino. Вам нужен опыт управления оборудованием напрямую с помощью языка C.
  * Я рекомендую купить комплект Atmega128 и реализовать программу для включения/выключения светодиодов, обнаружения входного сигнала переключателя и отображения сообщений на текстовом ЖК-дисплее. Программа управления двигателем тоже очень хороший проект: например, трассировщик линии.
  * В процессе реализации проекта вы можете обращаться к документациям сторонних библиотек, но не можете использовать их.
* Основы ядра Linux
  * Низкоуровневое программирование очень близко к операционной системе. Вы в тонкостях должны знать как устроена ОС.
  * Начните с драйверов
    * Прочтите [Linux Device Drivers](https://lwn.net/Kernel/LDD3/), [на русском](https://vk.com/wall-88981965_5256)
    * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * Прочтите [Разработка ядра Linux](https://www.google.com/search?q=%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0+%D1%8F%D0%B4%D1%80%D0%B0+Linux+%D0%BA%D0%BD%D0%B8%D0%B3%D0%B0), [на русском](https://proninyaroslav.gitbooks.io/linux-insides-ru/content/index.html) для понимания тонкостей работы ОС.
* Go to the professional field
  * If you want to be a professional Linux Kernel Developer
    * must read [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
      * Тогда попробуй сделать игрушечное ядро
      * [Learn operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
      * [Making your own kernel](http://wiki.osdev.org/Getting_Started)
      * Добавьте ссылку GitHub на ваше ядро в своем резюме (не забудьте написать подробное описание в сообщении о коммите).
    * Check the latest issues at https://lwn.net/ and join it.
      * Check "Recent kernel patches" at "https://lwn.net/Kernel/" or direct link https://lwn.net/Kernel/Patches
      * Find an interesting patch to you. Try to understand the source code. Of course it would be really difficult but try. You will be closer and closer whenever you try.
      * Build kernel and test it on your system. For example, performance test, stability test with LTP(https://linux-test-project.github.io/) or static code analysis tools inside of kernel.
      * Сообщайте о любых проблемах, если вы их обнаружите: предупреждения/ошибки компиляции, падение производительности, паника ядра/упс или любая другая проблема.
      * Если вы сделали всё правильно. Владелец патча напишет сообщение «Проверено»; тег с вашим именем.
      * Найдите свое имя в логах ядра в git
  * А также множество других направлений
    * Есть много областей, где может работать разработчик низкоуровневого программного обеспечения: безопасность, компилятор, прошивка, робот/автомобиль и т. д.


# <a name="Translation"></a>Перевод

Если вы хотите перевести эту страницу, пришлите мне запрос на включение. Я перечислю это здесь.

* [Китайский (Традиционный)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_tw.md)
* [Китайский(Упрощённый)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cn.md)
* [Португальский (Бразильский)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_pt.md)
* [Итальянский](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_it.md)
* [Чешский](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cz.md)
* [Русский(эта страница)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_ru.md)
* [Турецкий](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_tr.md)
* [Персидский](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_fa.md)
* [Испанский](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_es.md)


# <a name="who-am-i"></a>Кто я такой?

Вдохновляясь [google-interview-university](https://github.com/jwasham/coding-interview-university), мне бы хотелось поделиться опытом и показать путь к становлению программистом низкоуровневого программного обеспечения, потому что я обнаружил, что эти навыки стали не так распространены, как раньше.
Кроме того, многие студенты и новички спрашивают меня, как им стать разработчиками низкоуровневого программного обеспечения и инженерами ядра Linux в частности.

Для информации, у меня более 10 лет опыта в качестве низкоуровневого программиста, мой опыт включает:
* Программирование на ассмемблере под 80x86 
* Аппаратные средства на чипах Atmel и прошивки для них
* Язык C и системное программирование под Unix
* Драйвера устройств под Linux
* Ядро Linux: подкачка страниц
* Ядро Linux: драйвер блочного устройства и md module
<details>
      <summary>P.S</summary>
      множество книг при желании можно найти в свободном доступе
</details>