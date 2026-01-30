# VScode-Extensions-Download-Solution
Spoiler: Just a simple way to download VSCode Extensions while the usual installation directly from VSCode doesn't work in Russia.


Нажимаешь `install` на расширение в VSCode, а оно бесконечно виснет на загрузке?

VPN не помогал, но Я нашел как решить эту проблему. 

Моя система:

Windows 10 pro /
Kubuntu 24.04 LTS

Действия ниже приводятся с учётом того, что вы базово владеете вашей системой и без проблем решаете базовые проблемы, возникающие при работе с компьютером.

## WINDOWS:

Используем `vsixget`. Установка через pip:

```cmd
pip install vsixget
```

Потом ищем нужное нам расширение на маркетплейсе marketplace.visualstudio.com (можно с ВПН), смотрим нужный id формата `publisher.name`

И устанавливаем

```cmd
vsixget install publisher.name -d VSCodeExtensions/
```

*Флаг -d — директория скачивания. В этом примере команда создаст папку C:/VSCodeExtensions/*

Потом в VSCode заходим во вкладку `Extensions/Расширения` -> `Install from .VSIX` -> выбираем расширение в проводнике и скачиваем.

## UBUNTU:

Подобная ютилка есть и на любимой Ubuntu, работает так же, но называется vsix и качается через tar.gz архив с гитхаба. https://github.com/beeltec/vsix/releases/tag/v1.0.2

Затем в терминале:

```bash
cd Downloads
tar -xzf vsix-x86_64-linux.tar.gz
```

*Опционально: Если захотите, то можно перенести это в удобную для вас папку

Затем действия такие:
```bash
vsix search python
```

Причем, тут пока не сильно важно 100% верное написание, тут обычный поиск.

Смотрим на ID. В этом случае у нас `kilocode.Kilo-Code`.

Теперь вводим команду:

```bash
vsix install kilocode.Kilo-Code
```

И vsix сама скачает это расширение на ваш VSCode.

#### TODO:
В корне проекта есть папка examples с готовыми сборками для разных языков программирования. Вы можете доливать свои, предлагать наборы команд для `vsix`. 

# Да будет код писаться!
