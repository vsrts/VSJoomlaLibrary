# VSJoomlaLibrary
Connect your custom library and use it anywhere on Joomla CMS

Данный плагин для Joomla позволяет иметь доступ к своей библиотеке не только из конкретного расширения, но и из любой точки приложения. 

Плагин привязывается к событию «onAfterInitialise», которое срабатывает сразу после инициализации фреймворка Joomla.

В событии «onAfterInitialise» регистрируется префикс класса, по которому автозагрузчик будет искать классы вашей библиотеки.

Чтобы использовать метод registerPrefix() необходимо следовать определенному соглашению по именованию классов и файлов. Имя класса должно быть в camel case, где каждый сегмент имени представляет путь к папке, а последний сегмент является именем файла класса. Если в имени класса только одна часть, то автозагрузчик будет искать файл в папке с таким же названием. Названия папок должны быть в нижнем регистре.

Например:

Класс PrefixUserModel должен находиться в ПУТЬ_ДО_ПРЕФИКСА/user/model.php

Класс PrefixUser должен находиться в ПУТЬ_ДО_ПРЕФИКСА /user/user.php

