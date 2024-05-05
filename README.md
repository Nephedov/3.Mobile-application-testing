# Домашнее задание к занятию «Тестирование Android-приложений»

## Решения
### Задание 1
* <a href="https://docs.google.com/document/d/1NZCbx81gpMyjsG9jjpgOXWZ0NBbfuCz6zOqEiofFfT8/edit?usp=share_link">Геокешинг</a> - возможные причины и действия для их локализации.


### Задание 2
* <a href="https://docs.google.com/spreadsheets/d/1dryLFCcfyM3ejPDmtKkuucNLb7fMTZ9sAKsyDbujwjQ/edit?usp=share_link">Чек-лист</a> тестирования подписок приложения, с приоритетами. Включает 67 проверок.


### Задание 3
* <a href="https://docs.google.com/document/d/1WJiHSunr1Ob8aBDfdnDaND0vvMYnOd7p9hh2FICqvds/edit?usp=share_link">Документ</a> - с описанием областей применения в тестировании,
  разделов в режиме разработкчика android-устройства.

## Что было сделано
### Задание 1
* Составлен список возможных причин долгой обработки запроса и предполагаемых действий с устройством, для локализации причин -
  <a href="https://docs.google.com/document/d/1NZCbx81gpMyjsG9jjpgOXWZ0NBbfuCz6zOqEiofFfT8/edit?usp=share_link">Геокешинг</a>.

  
### Задание 2
* Реализован <a href="https://docs.google.com/spreadsheets/d/1dryLFCcfyM3ejPDmtKkuucNLb7fMTZ9sAKsyDbujwjQ/edit?usp=share_link">чек-лист</a> тестирования подписок приложения.


### Задание 3
* В режиме разработчика на android-устройстве были включены разделы:
    * Границы элементов.
    * Нажатия и касания. 
    * Настройка ANR.
    * Лимит фоновых процессов — максимум 1 процесс.
    * Установлено приложение Fake GPS Location и выбрано для фиктивных местоположений.
* Составлен <a href="https://docs.google.com/document/d/1WJiHSunr1Ob8aBDfdnDaND0vvMYnOd7p9hh2FICqvds/edit?usp=share_link">документ</a>
  с описанием областей применения в тестировании описанных выше функций и разделов. Содержит скриншоты с выбранными разделами.


## Описание Задания 1
Ваша команда разрабатывает новое приложение для [геокешинга](https://www.geocaching.com/).

Мобильное приложение подключено через API к Google Картам.

При тестировании первой стабильной сборки вы обнаружили проблему: 
- на вашем единственном тестовом Android-устройстве после установки и разрешения запроса на геолокацию запрос обрабатывается в течение приблизительно 7 сек.
У Android-разработчика на эмуляторе ничего не воспроизводится :)

Мы знаем, что службы геолокации обычно используют для определения местоположения GPS, Bluetooth, краудсорсинговые данные о точках доступа Wi-Fi и вышки сотовой связи. 

Ваше тестовое устройство — **Samsung Galaxy A12 (SM-A125) 4/64 ГБ RU, версия Android 10.**

**Что нужно сделать:**
- cформулируйте возможные причины такого поведения приложения на вашем устройстве;
- напишите, какие действия вы совершите с устройством в первую очередь, чтобы убедиться, что это точно не проблема устройства.


## Описание Задания 2
Продуктовая команда решила, что для нового Android-приложения музыкального стримминга будет использоваться подписочная модель монетизации.
Эта модель предлагает бесплатную демонстрационную trial-версию приложения и дальнейшую оплату использования на определённый срок с последующим автоматическим продлением.

**Условия:**

1. Доступны реккурентные продукты: подписка на 3 месяца и 1 год.
2. Каждому пользователю при подписке будет доступен бесплатный пробный период 30 дней, после которого будет списываться сумма полной подписки. 
3. Списание будет происходить за сутки до окончания срока действия пробного периода.
4. При нехватке средств в день продления сервер в течение суток дважды отправит запрос на списание. При двух неудачных попытках доступ будет закрыт.
5. 30 дней бесплатного доступа ко всем фичам планируется активно рекламировать при запуске приложения, но через 2 месяца уже запланировано изменение срока триального доступа с 30 дней на 15.
6. Важно учесть,что в Google Play возможна временная приостановка, полная отмена подписки и возобновление. Подробные детали можно узнать в документации от [Google](https://developer.android.com/google/play/billing/test).


**Что нужно сделать:**

- составить чек-лист тестирования подписок для приложения. 


## Описание Задания 3

Вы получили новый тестовый Android-девайс. 

Перед началом тестирования обязательно нужно включить на устройстве меню разработчика и функции в нём:  

- показывать границы элементов; 
- показывать нажатия и касания; 
- установить настройку ANR — уведомление о том, что приложение не отвечает;
- установить лимит фоновых процессов — максимум 1 процесс;
- установить приложение Fake GPS Location. В меню разработчика выбрать данное приложение для фиктивных местоположений.
