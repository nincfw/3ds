---
title: "Обновление boot9strap"
permalink: updating-b9s.html
author_profile: true
---
{% include toc title="Разделы" %}

<h3>Самая свежая версия b9s - 1.3 от 06.09.2017</h3>

Эта страница предназначена для пользователей boot9strap, чтобы они могли обновить установленный boot9strap до последней версии. Если у вас a9lh - перейдите на [b9s](a9lh-to-b9s). Если вы еще не прошили приставку, вернитесь в [начало гайда](/) и прошейте. 

{% capture notice-1 %}
Сообщается о волне банов, выданных Nintendo пользователям CFW. Чтобы защитить себя, выполните следующие шаги перед началом этого руководства:

1. Откройте Системные настройки, затем "Интернет-настройки", затем "SpotPass", затем "Отправка информации о системе"
1. Отключите опцию "Отправка информации о системе"
1. Закройте Системные настройки
1. Откройте Список друзей (значок в виде лица на верхней строчке меню Home)
  + Если появляется ошибка и вас не пускают в меню, значит Список друзей уже отключен
1. Перейдите в настройки Списка друзей, затем "Настройки сообщений друга", затем "Показать друзьям, во что вы играете"
1. Отключите опцию "Показать друзьям, во что вы играете"
1. Закройте Список друзей

{% endcapture %}

<div class="notice--danger">{{ notice-1 | markdownify }}</div>

## Что понадобится

* Свежая версия [Luma3DS](https://github.com/AuroraWright/Luma3DS/releases/latest) *(`.7z-архив`)*
* Свежая версия [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest)
* Свежая версия [boot9strap](https://github.com/SciresM/boot9strap/releases/latest) *(стандартный boot9strap; не `devkit-файл`, не `ntr-файл` и не `devkit-ntr-файл`)*
* Свежая версия [GodMode9](https://github.com/d0k3/GodMode9/releases/latest)
* Свежая версия [Luma3DS Updater](https://github.com/KunoichiZ/lumaupdate/releases/latest)
* Homebrew [Starter Kit](http://smealum.github.io/ninjhax2/starter.zip)
* [`setup_ctrnand_luma3ds.gm9`]({{ "/gm9_scripts/setup_ctrnand_luma3ds.gm9" | absolute_url }})
* [`cleanup_sd_card.gm9`]({{ "/gm9_scripts/cleanup_sd_card.gm9" | absolute_url }})

## Инструкция

#### Часть I - Определение версии загрузчика 
Сначала нужно определить каким методом приставка взломана. 

1. Отключите 3DS
1. Загрузите приставку с зажатой кнопкой (SELECT)
1. Обратите внимание на первую строчку, там написана версия Luma3DS
  + Если Luma3DS меньше, или равна 7.0.5, то у вас a9lh - выполняйте указания из этой инструкции, чтобы перейти на b9s актуальной версии
  + Если Luma3DS 7.1, то у вас b9s 1.0 и нужно [обновить его до актуальной версии](updating-b9s)
  + Если версия Luma3DS выше, или равна 8.0, у вас b9s 1.2 или выше. Можете [обновить его до актуальной версии](updating-b9s), если вы не знаете какая именно у вас стоит сейчас

    ![]({{ base_path }}/images/screenshots/luma.png)
	{: .text-center}
    {: .notice--info}

#### Часть II - Подготовительные работы

Для всех шагов в этой части перезаписывайте любые существующие файлы на SD-карте.
{: .notice--info}

{% capture notice-10 %}
**Не копируйте** в этой части boot.firm от Luma3DS 8, если у вас b9s 1.0! Если вы сделали это следуйте следующим рекомендациям: 
<br>
[Cкачайте Luma3DS 7.1](https://github.com/AuroraWright/Luma3DS/releases/tag/v7.1), и скопируйте boot.firm из архива с прошивкой на SD-карту, согласившись на замену. Обновление Luma3DS до актуальной версии будет произведено в следующей части. Если у вас b9s 1.2, то вреда от копирования не будет.
{: .notice--danger}
{% endcapture %}

<div class="notice--info">{{ notice-6 | markdownify }}</div>

1. Перейдите в Системные настройки (System Settings), Управление данными (Data Managment), Nintendo 3DS, Программы (Software) и удалите Luma3DS Updater
1. Выключите консоль
1. Вставьте SD-карту в компьютер
1. **Помните, что ещё не следует копировать boot.firm от Luma 8.0, мы сделаем это в следующей части**
1. Скопируйте _содержимое_ архива `starter.zip` в корень SD-карты **целевой 3DS**
1. Создайте папку `boot9strap` в корне SD-карты
1. Скопируйте `GodMode9.firm` из `.zip-архива` GodMode9 в папку `/luma/payloads/` на SD-карте
1. Скопируйте папку `gm9` из `.zip-архива` `GodMode9` в корень SD-карты
1. Скопируйте `setup_ctrnand_luma3ds.gm9` в папку `/gm9/scripts/` на SD-карте
1. Скопируйте `SafeB9SInstaller.firm` из `.zip-архива` SafeB9SInstaller в папку `/luma/payloads/` на SD-карте
1. Скопируйте `boot9strap.firm` и `boot9strap.firm.sha` из `.zip-архива` с boot9strap в папку `/boot9strap/` в корне SD-карты
1. Создайте папку `cias` в корне SD-карты
1. Скопируйте `lumaupdater.cia` в папку `/cias/` на SD-карте
1. Вставьте SD-карту обратно в консоль

#### Часть III - Обновление системы

Если прежде чем начать выполнять действия из этого руководства у вас уже был установлен EmuNAND и вы хотите перенести содержимое EmuNAND в SysNAND с кастомной прошивкой - сейчас самый подходящий момент. Выполните действия из раздела [перенос EmuNAND](move-emunand), перед выполнением этой части. Если EmuNAND у вас нет, или вы не знаете что это такое - просто следуйте руководству дальше. 
{: .notice--info}

1. Обновите прошивку консоли, зайдя в Системные настройки (System Settings), затем "Прочие настройки" (Other Settings), затем листайте ВПРАВО до конца и выберите пункт "Обновление" (System Update)
  + Обновление консоли с установленным B9S + Luma (установленых у вас) безопасно
  + При появлении ошибки, поставьте в настройках подключения, в настройках DNS "Получать DNS автоматически" в положение "Да"
  + Если вы все еще получаете ошибку [выполните CTRTransfer](ctrtransfer) и попробуйте обновиться еще раз

#### Часть IV - Установка boot9strap

1. Включите приставку, удерживая кнопку (START), чтобы запустить меню Luma3DS chainloader
1. Запустите SafeB9SInstaller, нажав кнопку (A)
1. Дождитесь окончания всех проверок безопасности
1. При появлении запроса, введите указанную комбинацию кнопок для установки boot9strap
1. После завершения процесса, нажмите (A) для перезагрузки
1. Выключите консоль, нажатием любой кнопки, **игнорируя ошибку**
  + Обратите внимание, что ошибка `Unsupported launcher (argc = 0)` будет появляться до тех пор, пока вы до конца не выполните инструкцию из этой страницы

#### Часть V - Обновление Luma3DS

1. Вставьте SD-карту в компьютер
1. Удалите файл `boot.firm` из корня SD-карты
1. Скопируйте файл `boot.firm` из `.7z-архива` Luma3DS в корень SD-карты
1. Вставьте SD-карту обратно в консоль

#### Часть VI - Настройка Luma3DS

Эта часть требуется только в том случае, если после перезагрузки появилось меню настроек Luma3DS.
{: .notice--info}

1. Включите приставку
1. Устройство загрузится в меню настройки Luma3DS
  + Если после включения экран остаётся чёрным, то перейдите к разделу [проблемы и их решения](troubleshooting#черный-экран-при-загрузке-sysnand-после-установки-b9s)
1. Нажимая (A) выберите следующие пункты:    
  + **"Enable game patching"**
  + **"Show NAND or user string in System Settings"**
1. Если у вас **New 3DS**, вы *также* можете включить следующие опции:
  + **"New 3DS CPU" выбрать значение "Clock+L2(x)"**
    + Это увеличит частоту кадров в множестве игр, но может отразиться на стабильности других
    + Если какие-либо игры работают некорректно, отключите эту опцию
	
    ![]({{ base_path }}/images/screenshots/luma-settings.png)
	{: .text-center}
    {: .notice--info}
	
1. Нажмите (START), чтобы сохранить настройки и перезагрузиться

#### Часть VII - Установка Luma3DS Updater

1. Запустите FBI
1. Перейдите в `SD` -> `cias`
1. Выберите `lumaupdater.cia`
1. Выберите "Install CIA", затем нажмите (A) для подтверждения
1. Нажмите (HOME) для выхода из FBI

#### Часть VIII - CTRNAND Luma3DS

Обратите внимание, что если у вас имеются другие файлы помимо `GodMode9.firm` в папке `/luma/payloads/` на SD-карте, удержание кнопки (START) при загрузке будет запускать "chainloader menu", где вам нужно будет использовать D-Pad и кнопку (A) для выбора "GodMode9" при выполнении этих инструкций.
{: .notice--info}

1. Запустите GodMode9, удерживая (START) во время включения приставки
1. Если вам предложат создать бэкап важных файлов, нажмите кнопку (A) чтобы сделать это, затем нажмите (A) чтобы продолжить после завершения
1. Если вам предложат выставить RTC дату и время, нажмите (A) чтобы сделать это, настройте дату и время, затем нажмите (A) чтобы продолжить
	+ Обратите внимание, что если вы выставили RTC дату и время, вам также придется настроить время в Системных настройках после этого руководства
1. Нажмите (HOME), чтобы попасть в меню действий
1. Выберите "Scripts..."
1. Выберите "setup_ctrnand_luma3ds"
1. Когда появится запрос, нажмите (A) для подтверждения
1. Нажмите (A), чтобы разрешить запись в SysNAND (lvl1) и введите указанную комбинацию кнопок
1. Нажмите (A) чтобы продолжить
1. Нажмите (A) чтобы вновь заблокировать права на запись

##### Часть IX - Очистка SD-карты

Помните, что скрипт, используемый ниже, удалит папки `/boot9strap/` и `/cias/` с SD-карты!
{: .notice--danger}

1. Нажмите кнопку (HOME) для вызова меню
1. Выберите "Scripts..."
1. Выберите "cleanup_sd_card"
1. При появлении запроса, нажмите (A) для продолжения
1. Нажмите (A), чтобы продолжить
1. Нажмите (START) для перезагрузки

После работы скрипта корень SD-карты будет выглядеть следующим образом: 

![]({{ base_path }}/images/screenshots/final-file-layout.png)
{: .text-center}

__

{% capture notice-10 %}
Теперь вы можете использовать Luma3DS Updater для обновления кастомной прошивки. Запустите его и нажмите (А).     
Это не тоже самое что Обновление системы (System Update). Это приложение обновляет только файлы Luma3DS.
Это обновит только те файлы Luma3DS, которые находятся на SD-карте. Если вы включите консоль без SD-карты, она загрузится используя Luma3DS из CTRNAND.    
{% endcapture %}

<div class="notice--info">{{ notice-10 | markdownify }}</div>

{% capture notice-6 %}   
Теперь нажатие (L) + (ВНИЗ) + (SELECT) в запущенной системе открывает меню Rosalina, встроенное в Luma3DS. Полный список функций Rosalina можно найти тут: [Luma3DS v8.0 Release](https://github.com/AuroraWright/Luma3DS/releases/tag/v8.0) (англ.) и немного вольный [перевод на русский](https://vk.com/3ds_cfw?w=wall-125012133_5360)
{% endcapture %}

<div class="notice--info">{{ notice-6 | markdownify }}</div>

Для использования [NTR CFW](https://github.com/44670/BootNTR/), установите [BootNTR Selector](https://gbatemp.net/threads/432911/).
{: .notice--info}

<div class="notice--info">{{ notice-7 | markdownify }}</div>

Для получения информации по использованию различных функций GodMode9 обратитесь к разделу [Использование GodMode9](godmode9-usage).
{: .notice--success}

Для справки об использовании различных функций Luma3DS обратитесь к её [вики](https://github.com/AuroraWright/Luma3DS/wiki/Options-and-usage) (англ.).
{: .notice--success}

Различные инструкции, не имеющие прямого отношения ко взлому, однако помогающие лучше изучить возможности 3DS на кастомной прошивке и эффективнее ей пользоваться находятся [здесь](addons).
{: .notice--success}
