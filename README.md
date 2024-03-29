# ЛР 2
## Коновалов А.С. М3О-312Б-18.

### Постановка задачи
1. Выведите на экран листинг характеристик (в длинном и коротком форматах) процессов, инициализированных с Вашего терминала. Проанализируйте и объясните содержание каждого поля сообщения.
2. Выведите на экран листинг характеристик всех процессов. Используйте при необходимости конвейер с more для постраничного просмотра листинга. Какой процесс является родительским для большинства процессов? Что означает символ ? в поле управляющий терминал процесса?
3. Выведите на экран листинг процессов, запущенных конкретным пользователем. Какой ключ пришлось использовать? Что говорит значение ? в поле управляющий терминал процесса?
4. Разработайте и запустите простейшую процедуру в фоновом режиме с бесконечным циклом выполнения, предусматривающую, например, перенаправление вывода каких-то сообщений в файл или в фиктивный файл, и использующую команду sleep для сокращения частоты циклов процедуры.
5. Выполните п. 1. Объясните изменения в листинге характеристик процессов.
6. Понизьте значение приоритета процедуры. На что и как повлияет эта операция при управлении вычислительным процессом системы? Как отразятся ее результаты в описателях процессов?
7. Проанализируйте листинг процессов. Какой процесс является родительским для процедуры.
8. Выйдите из системы и войдите заново. Проанализируйте листинг процессов. Объясните изменения в системе.
9. Запустите процедуру в фоновом режиме, но предусмотрите ее защиту от прерывания при выходе из системы.
10. Выполните п.6. Объясните изменения PPID процедуры.
11. Завершите выполнение процесса процедуры.
12. Запустите процедуру в интерактивном режиме с перенаправлением вывода в соответствующий файл.
13. Переведите задание с процедурой в фоновый режим и проанализируйте сообщение на экране. Что пришлось дополнительно сделать? Как выглядят приостановленные процессы в листинге команды ps?
14. Переведите задание с процедурой в интерактивный режим и проанализируйте сообщение на экране.
15. Завершите выполнение процедуры и проанализируйте сообщение на экране

### Практическая часть:

1. Выводим в окно терминала листинг характеристик процессов в коротком формате 

![Screenshot_1](https://user-images.githubusercontent.com/55550028/120068387-175dae00-c089-11eb-830e-2b99813df76b.png)

Поле PID означает идентификатор процесса. Поле TTY означает имя иерминала с которого запущен процесс. Поле TIME означает процессорное время, затраченное на выполнение данного процесса. Поле CMD означает команду которая вызвала выполнение процесса
Выведем на окно терминала листинг характеристик процессов в длинном формате:

![Screenshot_2](https://user-images.githubusercontent.com/55550028/120068443-63a8ee00-c089-11eb-9ae4-b962a56dcb5d.png)

Вывод дополнился новыми полями. Поле UID означает идентификатор пользователя, который запустил процесс. Поле PPID означает идентификатор родительского процесса. Поле STIME означает время старта процесса. Вывод дополнился новыми полями. Поле UID означает идентификатор пользователя, который запустил процесс. Поле PPID означает идентификатор родительского процесса. Поле STIME означает время старта процесса.
2. Выводим листинг характеристик всех процессов при помощи команды ps ax -f:

![Screenshot_3](https://user-images.githubusercontent.com/55550028/120068452-702d4680-c089-11eb-8870-c498a4b91022.png)

3. Чтобы вывести листинг процессов для определенного пользователя, выйдем из пользователя "root" 

![Screenshot_4](https://user-images.githubusercontent.com/55550028/120068486-99e66d80-c089-11eb-9a4f-09bee4689f55.png)

4. Воспользуемся редактором "vi" и создадим программу с помощью команды "vi s.py": Перейдем в режив ввода нажатием клавиши "i" и введем текст программы:

![Screenshot_5](https://user-images.githubusercontent.com/55550028/120068498-aa96e380-c089-11eb-9b2a-197b6246eea2.png)

Сохраним и выйдем из редактора
Запустим программу из терминала в фоновом режиме: [artem@localhost]# python s.py & 
5. Выведем листинг характеристик процессов root@localhost]# ps -f

![Screenshot_7](https://user-images.githubusercontent.com/55550028/120068580-0cefe400-c08a-11eb-8c59-2d75c5f8f779.png)

6. Понизим приоритет процесса 1392 до значения 5 и выведем характеристику процессов с ключом "l":

![Screenshot_8](https://user-images.githubusercontent.com/55550028/120068591-18430f80-c08a-11eb-89ce-9abe108f2a7b.png)

7.  Родительским процессом для процесса 1251 является процесс с идентификатором 1247 - bash.

8.  Выйдем из системы командой "exit" и зайдем заново 
9.  Запустим процедуру в фоновом режиме и предусмотрим ее защиту от прерывания.

![Screenshot_10](https://user-images.githubusercontent.com/55550028/120068613-33158400-c08a-11eb-85ec-6dacf103b01e.png)

10.  Выведим листинг характеристик процессов

![Screenshot_11](https://user-images.githubusercontent.com/55550028/120068620-3f014600-c08a-11eb-9851-333c53c87197.png)

11.   Переведем процедуру в интерактивный режим:
[root@localhost]# fg 
```sh
python s.py
```

Вывод: В ходе лабораторной работы были изучены команды для работы с процессами в операционной системе Linux, а так же проведена работа с текстовым редактором vi.
