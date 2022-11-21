# TRiTPO-lab2
# Требования к проекту 

Содержание
=================
* 1 [Введение](#1-введение)
* 2 [Требования пользователя](#2-требования-пользователя)
  * 2.1 [Программные интерфейсы](#21-программные-интерфейсы)
  * 2.2 [Интерфейс пользователя](#22-интерфейс-пользователя)
  * 2.3 [Характеристики пользователей](#23-характеристики-пользователей)
* 3 [Системные требования](#3-системные-требования)
  * 3.1 [Функциональные требования](#31-функциональные-требования)
  * 3.2 [Нефункциональные требования](#32-нефункциональные-требования)


## 1. Введение
Название - FsFilter.

Данный драйвер предоставляет информацию о всех действиях файловой системы Windows в лог ядра. Как и любой драйвер, драйвер-фильтр должен предоставлять функции загрузки и выгрузки драйвера, затем в обязательном порядке все драйвера файловой системы должны зарегистрировать координирующую таблицу ввода/вывода и сам механизм регистрации обращений к файловой системе, который и будет выводить в отладочный модуль ядра активность файловой системы. Также важно организовать передачу запроса другим драйверам, состоящих в цепи обработки запроса. Это все основные структурные единицы драйвера-фильтра, которые необходимы для корректной работы драйвера.

## 2. Требования пользователя

### 2.1 Программные интерфейсы
Для получения информации о логах ядра Windows необходима программа DebugView. 

### 2.2 Интерфейс пользователя

Окно вывода приложения при запуске драйвера. 

![image](https://github.com/Nikitos126/TRiTPO-lab2/blob/main/Mockups/%D0%91%D0%B5%D0%B7%D1%8B%D0%BC%D1%8F%D0%BD%D0%BD%D1%8B%D0%B9.png)

Для проверки вывода сообщений данного драйвера необходимо запустить прогрумма DebugView, в которой можно отслеживать информацию, которую выводит фильтр-драйвер в лог ядра Windows. 

![image](https://github.com/Nikitos126/TRiTPO-lab2/blob/main/Mockups/Debug.png)

Окно вывода приложения при закрытии драйвера.

![image](https://github.com/Nikitos126/TRiTPO-lab2/blob/main/Mockups/Unload.png)

### 2.3 Характеристики пользователей
Данное приложение могут использовать пользователи компьютеров с операционной системой Windows 10.

## 3. Системные требования
Операционная система Windows 10, минимальная версия 1507.
### 3.1 Функциональные требования
Должны быть реализованы следующие возможности:
1. Коректная установка драйвера и вывод информации о его загрузке.
2. При запуске драйвера должна выводится информация об успешном его запуске.
3. Вывод информации от драйвера в лог ядра об открытых файлах и директориях.
4. При прекращении работы драйвера выводится информация об его остановке.
5. Выгрузка драйвера и вывод сообщения об успешном его удалении.

### 3.2 Нефункциональные требования
1. Использование программы DebugView 
2. Пошаговая инстукция по использованию драйвера представлена в справке.
