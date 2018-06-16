---
title: "Создание movable_part1 (seedminer)"
permalink: /seedminer-ms1.html
author_profile: true
---

{% include toc title="Разделы" %}

Способ получения movable_part1.sed может отличаться в зависимости от того какими средствами вы владеете. 

## 	Выберите способ, который больше всего подходит лично вам:

**Способ I - если у вас есть возможность запустить Homebrew Launcher на вашей приставке**

{% capture notice-1 %}
Если у вас есть возможность запустить Homebrew Launcher на приставке, что вы собираетесь прошить, обратитесь к этому способу. Подробнее об альтернативных точках входа можно [почитать здесь](homebrew-launcher-alternatives){:target='_blank'}. 

[Перейти к Способу I](/seedminer-ms1#%D0%A1%D0%BF%D0%BE%D1%81%D0%BE%D0%B1-i---%D1%81-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%D0%BC-homebrew-launcher-%D0%BD%D0%B0-%D0%B2%D0%B0%D1%88%D0%B5%D0%B9-%D0%BF%D1%80%D0%B8%D1%81%D1%82%D0%B0%D0%B2%D0%BA%D0%B5)
{% endcapture %}
<div class="notice--success">{{ notice-1 | markdownify }}</div>

___

**Способ II - если у вас есть возможность запустить Homebrew Launcher на другой приставке**

{% capture notice-2 %}
Этот способ подойдёт тем, у кого есть вторая прошитая консоль (работает и не прошитая, главное, чтобы можно было запустить Homebrew Launcher), либо друг с таковой и есть компьютер на Windows и достаточно хорошая видеокарта.
 Для того, чтобы использовать этот метод, вы должны обменяться кодами друзей (Friend Code). Если не знаете как это сделать - обратитесь к инструкции консоли, или в [Google](http://google.com){:target='_blank'}. 

[Перейти к Способу II](/seedminer-ms1#%D0%A1%D0%BF%D0%BE%D1%81%D0%BE%D0%B1-ii---%D1%81-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%D0%BC-homebrew-launcher-%D0%BD%D0%B0-%D0%B4%D1%80%D1%83%D0%B3%D0%BE%D0%B9-%D0%BF%D1%80%D0%BE%D1%88%D0%B8%D1%82%D0%BE%D0%B9-%D0%BF%D1%80%D0%B8%D1%81%D1%82%D0%B0%D0%B2%D0%BA%D0%B5)
{% endcapture %}
<div class="notice--success">{{ notice-2 | markdownify }}</div>

___

**Способ III - если у вас вообще нет возможность запустить Homebrew Launcher ни на своей, ни на чужой приставке**

{% capture notice-3 %}
В этом методе мы полностью полагаемся на силу сообщества и будем использовать ресурсы и время волонтёров, которые помогают безвозмездно взлому консолей незнакомых людей. 

[Перейти к Способу III](/seedminer-ms1#%D0%A1%D0%BF%D0%BE%D1%81%D0%BE%D0%B1-iii---%D1%81-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%D0%BC-%D1%82%D0%BE%D0%BB%D1%8C%D0%BA%D0%BE-%D0%B2%D0%B0%D1%88%D0%B5%D0%B9-%D0%BF%D1%80%D0%B8%D1%81%D1%82%D0%B0%D0%B2%D0%BA%D0%B8-%D0%B1%D0%B5%D0%B7-%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA%D0%B0-homebrew-launcher)
{% endcapture %}
<div class="notice--success">{{ notice-3 | markdownify }}</div>

___

### Способ I - с использованием Homebrew Launcher на вашей приставке 

Этот способ подойдёт тем, у кого есть вторая прошитая консоль (работает и не прошитая, главное, чтобы можно было запустить Homebrew Launcher), либо друг, с таковой и есть компьютер на Windows и достаточно хорошая видеокарта.
 Для того, чтобы использовать этот метод, вы должны обменяться кодами друзей (Friend Code). Если не знаете как это сделать - обратитесь к инструкции консоли, или в [Google](http://google.com){:target='_blank'}. 

1. Распакуйте `zip-архив` с seedminer на ваш ПК
1. Скопируйте `seedstarter.3dsx` в папку 3ds на SD-карте вашей приставки и вставьте её в консоль
1. [Запустите Homebrew Launcher](homebrew-launcher-alternatives){:target='_blank'} и выберите seedStarter
1. Нажмите {% include inc/btn.txt btn="A"%} для того, чтобы сделать дамп LFCS 
1. Нажмите {% include inc/btn.txt btn="A"%}, а затем {% include inc/btn.txt btn="START"%}, чтобы выйти из программы в HBL
1. Вставьте SD-карту приставки в компьютер
1. Скопируйте `movable_part1.sed` из папки `seedstarter` на SD-карте в папку `seedminer`, которую мы извлекли из `zip-архива` с seedminer на первом шаге.

Следующий шаг: [Подбираем movable.sed](seedminer-ms)
{: .notice--success}

___

### Способ II - с использованием Homebrew Launcher на другой прошитой приставке

Рекомендуется воспользоваться [Cпособом III](/seedminer-ms1#%D0%A1%D0%BF%D0%BE%D1%81%D0%BE%D0%B1-iii---%D1%81-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%D0%BC-%D1%82%D0%BE%D0%BB%D1%8C%D0%BA%D0%BE-%D0%B2%D0%B0%D1%88%D0%B5%D0%B9-%D0%BF%D1%80%D0%B8%D1%81%D1%82%D0%B0%D0%B2%D0%BA%D0%B8-%D0%B1%D0%B5%D0%B7-%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA%D0%B0-homebrew-launcher) для генерации movable_part1.sed, даже если у вас есть возможность запуска HBL на другой консоли, поскольку он много быстрее и проще. Вернитесь к этому способу только если у вас возникнут проблемы при использовании Способа III. 

Этот способ подойдёт тем, у кого есть вторая прошитая консоль (работает и не прошитая, главное, чтобы можно было запустить Homebrew Launcher), либо друг с таковой. Для того, чтобы использовать этот метод, вы должны обменяться кодами друзей (Friend Code). Если не знаете как это сделать - обратитесь к инструкции консоли, или в [Google](http://google.com){:target='_blank'}. 

**Проделайте это на приставке у которой есть доступ к Homebrew Launcher:**
1. Распакуйте `zip-архив` с seedminer на ваш ПК
1. Скопируйте `seedstarter.3dsx` в папку "3ds" на SD-карте вашей приставки и вставьте её в консоль
1. [Запустите Homebrew Launcher](homebrew-launcher-alternatives){:target='_blank'} и выберите seedStarter
1. Нажмите {% include inc/btn.txt btn="B"%} для того, чтобы сделать дамп LFCS 
1. Нажмите {% include inc/btn.txt btn="A"%}, а затем {% include inc/btn.txt btn="START"%}, чтобы выйти из программы в HBL
1. Вставьте SD-карту приставки в компьютер
1. Перейдите в папку `seedstarter/LFCS` 
1. Скопируйте `Y_XXXX-XXXX-XXXX_part1.sed` в папку `Nintendo 3DS` на SD-карте приставки, которую вы собираетесь прошивать (*XXXX-XXXX-XXXX* - код друга (Friend Code) той приставки которую мы прошиваем) 
	* Нужный Код друга (Friend Code) можно посмотреть на приставке, которую вы собираетесь прошивать. Откройте Список друзей (на нижнем экране верхний ряд иконок, оранжевая иконка с улыбкой). Ваш код будет написан на пиктограмме вашего Mii с короной.
	
	![]({{ base_path }}/images/seedminer/fc.png){:target="_blank"}
	{: .text-center}
	{: .notice--info}
	
1. Переименуйте `Y_XXXX-XXXX-XXXX_part1.sed` в `movable_part1.sed`
1. Скопируйте файл `seedminer_launcher3.py`, из папки с seedminer из первого пункта, в папку `Nintendo 3DS` на SD-карте приставки, которую вы собираетесь прошивать. 
	* Убедитесь, что в папке `Nintendo 3DS` есть только одна папка, состоящая из 32-х символов (ID0). Если таковых несколько, удалите те, что не являются папками вашей текущей учетной записи. Наверняка убедится можно, вставив в приставку другую SD-карту и дождавшись, пока консоль создаст на ней новую папку `Nintendo 3DS` с содержимым. Созданная папка, состоящая из 32-х символов (ID0), и будет искомой. Так же можно посмотреть на дату изменения папок. Более свежая, как правило, ваша. Имейте ввиду, что если на консоли стоит неверная дата, то дата изменения папки может быть неверной.
1. Запустите командную строку в папке `Nintendo 3DS` (вызовите контекстное меню с зажатой клавишей Shift, нажав на свободное место в папке, и выберите "Открыть Командную строку здесь" или "Открыть окно PowerShell здесь") и наберите в ней команду `py -3 seedminer_launcher3.py ID0`

	![]({{ base_path }}/images/seedminer/add_id0.png){:target="_blank"}
	{: .text-center}
	{: .notice--info}
	
1. Скопируйте `movable_part1.sed` из папки `seedstarter` на SD-карте в папку `seedminer`, которую мы извлекли из `zip-архива` с seedminer на первом шаге.

Следующий шаг: [Подбираем movable.sed](seedminer-ms)
{: .notice--success}

___

### Способ III - с использованием только вашей приставки, без запуска Homebrew Launcher

В этом методе мы полностью полагаемся на силу сообщества и будем использовать ресурсы и время волонтёров, которые помогают безвозмездно взлому консолей незнакомых людей. 

1. Распакуйте `zip-архив` с seedminer на ваш ПК
1. Перейдите на сайт [https://seedhelper.figgyc.uk/](https://seedhelper.figgyc.uk/){:target='_blank'}.
1. Введите в первое поле свой френдкод (только числа)
1. Введите во второе поле свой ID0, который мы получили чуть ранее
1. Нажмите Go и подождите пока страница изменится
	* Время ожидания может быть разным. Может пройти и несколько секунд и несколько часов (обычно не проходит больше минуты)
	* Если прогрессбар движется, значит страница не зависла и все идёт своим чередом
1. Вам высветился френдкод, добавьте его во Friend List на своей консоли
1. Страница изменится ещё раз. Нажмите на `download movable_part1.sed`, чтобы сохранить свой `movable_part1.sed` на ПК
1. Скопируйте `movable_part1.sed`  в папку `seedminer`, которую мы извлекли из `zip-архива` с seedminer на первом шаге.
1. Если вы планируете добывать ключ через этот же сайт, не закрывайте его и не обновляйте страницу

Следующий шаг: [Подбираем movable.sed](seedminer-ms)
{: .notice--success}