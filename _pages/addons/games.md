---
title: "Установка приложений"
permalink: /games.html
author_profile: true
---
{% include toc title="Разделы" %}

## Что понадобится

Если вы купили приставку у меня (в [VK](https://vk.com/market-125012133) или на [OLX](https://www.olx.ua/list/user/1nlHd/)), то у вас уже b9d со всеми необходимыми программами. Ищите их в папке Система (System)
{: .notice--info}

* Установленный и рабочий [b9s](updating-b9s) последней версии 
* Установленный и рабочий [FBI](fbi)
* Установленный [freeshop](finalizing-setup#freeshop)
* Свежая версия [BOOP](https://github.com/miltoncandelero/Boop/releases/latest) (запускается на вашем ПК)

## Инструкция

Инструкция работает для любой прошитой консоли с a9lh и b9s на борту.        
Есть два основных способа установки игр. Оба способа работают с файлами формата CIA. Разберем каждый из способов по отдельности.
{: .notice--info}

## Способ I - freeshop

1. Запустите freeshop
1. Нажмите на кнопку с пиктограммой лупы (нижний экран)
1. Введите в поиске название игры, или его фрагмент, и нажмите (A)
1. Выберите необходимую игру с помощью D-Pad и нажмите (X) для установки, либо (Y) для установки в фоне
1. На нижнем экране возле иконки со стрелкой появится цифра. С каждой новой поставленной в очередь установки игрой, цифра будет расти. Если нажать на эту иконку, увидите очередь загрузки
1. Если нажать на иконку с джойстиком, появится список уже установленных игр

Если около игры стоит желтый !, то для этой игры есть DLC. Если зеленый - обновление. Нажатие на соответствующую иконку, добавит выбранное дополнение в очередь загрузки
{: .notice--info}

## Способ II - FBI

#### Установка с SD-карты

1. Вставьте SD-карту в ПК
1. Создайте папку `games` в корне SD-карты
1. Вставьте SD-карту в консоль и включите её
1. Запустите FBI
1. Перейдите в папку `SD`
1. Перейдите в папку `games`
1. Наведите курсор на необходимую игру и нажмите (A)
1. Выберите `Install CIA` для установки игры, либо `Install and delete` для установки и автоматического последующего удаления `.cia-файла`
1. По завершению установки нажмите (A) и закройте FBI 
1. Установленное приложение появится в меню Home. 

Можно установить все файлы из папки. Для этого следует выбрать самую верхнюю строку - `<current directory>`, нажать на ней (А), а затем выбрать необходимое действие. 
{: .notice--info}

#### Установка с помощью QR-кода 

Если у вас нет указанных пунктов, обновите FBI! Для этого воспользуйтесь пунктом "Update" в его меню. В случае, если FBI у вас установлен с помощью инъекции в приложение "Информация о здоровье и безопасности" (Health & Safety), то при обновлении его иконка дублируется. Для того, чтобы этого избежать, восстановите приложение ["Информация о здоровье и безопасности"](https://3ds.customfw.xyz/godmode9-usage#восстановление-приложения-информация-о-здоровье-и-безопасности)
{: .notice--info}

1. Запустите FBI
1. Выберите пункт "Remote Install", а затем "Scan QR code" 
1. Отсканируйте необходимый QR-код 

#### Установка с ПК по беспроводному соединению

1. Запустите FBI
1. Выберите пункт "Remote Install", а затем "Recive URLs over the network" 
1. Запускаем Boop.exe
1. В открывшемся окне снимите галочку с пункта "Magically gues 3DS IP adress?"
1. В графе 3DS IP Adress введите IP, написанный на нижнем экране приставки. 
1. Убедитесь, что в графе "Computer IP Adress" указан именно ваш локальный IP (обратитесь в [Google](http://bfy.tw/D0PN), если не знаете как его узнать)
1. Перетащите CIA, которые вы хотите установить в приставку в окно программы, либо выберите их, нажав на кнопку "Pick files"
1. Нажмите на кнопку "BOOP"
1. На нижнем экране 3DS должны появиться две кнопки. Нажмите на (A) для подтверждения установки. 
  + Если кнопки не появились, убедитесь, что в программе стоит верный IP и нажмите кнопку "BOOP". Может понадобится несколько попыток

Важно понимать, что скорость установки программ таким способом не очень высокая и ограничивается примерно 500KBps для old3ds и 1.5Mbps для New. 
{: .notice--info}

## Где брать игры? 
1. [freeshop](finalizing-setup#freeshop)
2. [3dsisos](http://www.3dsiso.com/forumdisplay.php?261-CIA-Downloads)
3. [Все игры на русском](https://cloud.mail.ru/public/FfNX/u1oCpVmf3) от [VK: skotnikovnn](https://vk.com/skotnikovnn)
4. [Конвертировать .3DS-ромы в .CIA](https://3ds.customfw.xyz/godmode9-usage#convert_3ds)