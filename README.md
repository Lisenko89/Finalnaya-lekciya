### Тест план. 

#### Объект тестирования: форма [записи](https://netology.ru/programs/qa) на обучение профессии "Тестировщик ПО" на веб-сайте [Нетологии](https://netology.ru/).
#### Цель тестирования: автоматизация тестирования сценария перехода к форме [записи](https://netology.ru/programs/qa) и заполнения этой формы.

#### 1. Перечень автоматизируемых сценариев:

 #### 1.1 Переход к форме записи:

Для открытия стартовой страницы Нетологии https://netology.ru/
к переходу к форме записи https://netology.ru/programs/qa есть несколько вариантов, например:

+ Открыть [страницу Нетологии](https://netology.ru/) -> в заголовке слева, кликнуть вкладку "Каталог курсов" в всплывающем окне навести курсор на программирование, всплывающее окно меняет содержание, в столбце НЕО - выбрать "Тестировщик ПО" и перейти, на открывшейся странице: [страницу] (https://netology.ru/programs/qa) -> кликнуть кнопку "Записаться";
 
+ Открыть [страницу Нетологии](https://netology.ru/) -> в заголовке слева, кликнуть вкладку "Каталог курсов", в всплывающем окне выбрать "Полный каталог курсов, в открывшийся странице (https://netology.ru/navigation) выбрать "Тестировщиек ПО" и перейти, на открывшейся странице: [страницу] (https://netology.ru/programs/qa) -> кликнуть кнопку "Записаться"

+ Открыть [страницу Нетологии](https://netology.ru/) -> в разделе "Направления обучения" выбрать "Программирование" и перейти по нему, в открывшейся странице (https://netology.ru/development)  выбратьвыбрать "Тестировщик ПО" и перейти, на открывшейся странице: [страницу] (https://netology.ru/programs/qa) -> кликнуть кнопку "Записаться";

 
+ Открыть [страницу Нетологии](https://netology.ru/) -> пролистать страницу вниз до футера, в колонке "Обучение" выбрать "Программирование" и перейти по нему, в открывшейся странице (https://netology.ru/development)  выбратьвыбрать "Тестировщик ПО" и перейти, на открывшейся странице: [страницу] (https://netology.ru/programs/qa) -> кликнуть кнопку "Записаться"; 


  #### 1.2 Отправка формы:
   > Требования к содержимому полей:
    
  `Поле имя - в поле допускается заполнение кириллицей и латиницей, разрешены дефисы и пробелы, минимум два символа;`
  
     `Поле телефон - разрешены только цифры (11 цифр), символ + (вначале ввода);`
    
     `Поле электронная почта - допускается заполнение латиницей, цифрами и символами, поле должно содержать локальную часть адреса, знак "собаку" ( @ ) и доменную часть имени с точкой (.).`
     
    
   | Отправка формы                                               |  Результат                                                                     |
   |--------------------------------------------------------------|--------------------------------------------------------------------------------|
   |__Заполнение формы валидными значениями:__ заполнение полей валидными данными, отправка формы.  |данные успешно отправлены и могут быть просмотрены в соотвествующей базе данных;появится всплывающее окно об успешном завершении записи.|
   |                                                              |                        |
   |__Отправка пустой формы:__ отправка пустой формы|отправка данных не происходит; под незаполнеными полями отображается сообщение "Обязательное поле".| 
   |                                                              |                                                                                        |
   |__Отправка формы с пустым полем "Имя":__ поле "Имя" остается пустым, остальные поля заполняются валидными данными, отправка формы.|отправка данных не происходит; под незаполненын полем с сообщение "Обязательное поле".|
   |                                                              |                                                                                       |
   |__Отправка формы с пустым полем "Телефон":__ поле "Телефон" остается пустым, остальные поля заполняются валидными данными, отправка формы..|отправка данных не происходит; под полем телефон отображается сообщение "Обязательное поле".|
   |                                                               |                                                                                      |
   |__Отправка формы с пустым полем "Электронная почта":__ поле "Электронная почта" остается пустым, остальные поля заполняются валидными данными, отправка формы.|отправка данных не происходит; под полем "Электронная почта" отображается сообщение "Обязательное поле".|
   |                                                               |                                                                                                |
   |__Валидация каждого из полей формы, в случае ввода НЕвалидных данных, проверка на отображение соотвествующих ошибок:__|                                     |
   |                                              |                                              |
   |поле "Имя" заполняется невалидными данными, остальные поля заполняются валидными данными, отправка формы.|отправка данных не происходит; под полем "Имя" отображается сообщение: "Должно состоять из русских букв, дефисов и пробелов".|
   |                                              |                                                |
   |поле "Имя" заполняется одним буквенным символом, остальные поля заполняются валидными данными, отправка формы.|отправка данных не происходит; под полем "Имя" отображается сообщение: "Должно быть не короче 2 символов".|
   |                                              |                                                 |
   |поле "Телефон" заполняется невалидными данными, остальные поля заполняются валидными данными, отправка формы.|отправка данных не происходит; под полем "Телефон" отображается сообщение: "Номер в формате +9 (999) 999-99-99".|
   |                                                 |                                                  |
   |поле "Электронная почта" заполняется невалидными данными, остальные поля заполняются валидными данными, отправка формы.|отправка данных не происходит; под полем "Электронная почта" отображается сообщение: "Неверный email".|
   |                                                 |                                                  |
   |__Отправка формы с данными из ранее успешно отправленой формы:__ заполнение полей ранее успешно отправленными валидными данными,  отправка формы.|данные отправлены; отображается всплывающее окно о ранее созданной записи.| 

 
#### 2. Перечень используемых инструментов с обоснованием выбора:
 
+ IntelliJ IDEA, удобная среда подготовки авто-тестов;
+ JDK 11 или выше, т.к. потребуются инструменты работающие с Java;
+ JUnit Jupiter, инструмент автоматизированного тестирования;
+ Selenide, инструмент при тестировании веб-интерфейса;
+ Faker, для генерации данных при отправке формы;
+ MySQL, для просмотра базы данных;
  если будет предостален "слепок" SUT, то необходим доступ к удаленному серверу с предустановленными:
  - [x] GIT
  - [x] Docker
  - [x] Bash
   
  для развертывания SUT и базы данных;
+ GIT, в качестве хранилища авто-тестов.
 
#### 3. Перечень необходимых разрешений/данных/доступов:
+ необходимо письменное разрешение на проведение тестирования администрации веб-сайта Нетологии;
+ необходим доступ к базе данных записи на обучение профессии "Тестировщик ПО":
  либо к действующей базе данных (что всегда несет риски);
  либо "слепок" SUT, готовый к интеграции с пустой базой данных (либо "слепок" SUT и данные для интеграции с пустой базой данных).
  
#### 4. Перечень и описание возможных рисков при автоматизации:
+ зависимость авто-тестов от текущей реализации веб-элементов, даже не значительное их изменение может привести к падению авто-тестов;
+ авто-тесты не проверяют графическую составляющую, а именно едет ли верстка при тех или иных действиях, комфортна ли выбранная цветовая схема оформления и тд.

#### 5. Перечень необходимых специалистов для автоматизации:
+ при доступе к реальной базе данных достаточно одного тестировщика ПО;
+ при работе со "слепком" SUT, необходим человек который его подготовит, при необходимости предоставит данные для развертывания SUT и интеграции с базой данных.

#### 6. Интервальная оценка с учётом рисков (в часах):
+ для осуществления этого плана автоматизации, ориентировочно потребуется 24 рабочих часа.
