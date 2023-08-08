# Моя настройка Mac

Этот репозиторий содержит все приложения / инструменты / настройки, которые я использую на своём Mac.

#### Быстрая навигация
- [Моя настройка Mac](#моя-настройка-mac)
			- [Быстрая навигация](#быстрая-навигация)
	- [Системные настройки](#системные-настройки)
		- [Мышь](#мышь)
		- [Клавиатура](#клавиатура)
			- [Клавиши](#клавиши)
			- [Ввод текста](#ввод-текста)
	- [Homebrew / Terminal / Shell](#homebrew--terminal--shell)
		- [Homebrew](#homebrew)
		- [Terminal](#terminal)
		- [Shell](#shell)
			- [Fig](#fig)
			- [Плагины, которые использую](#плагины-которые-использую)
			- [Дополнения](#дополнения)
			- [Git](#git)
	- [Визуал и продуктивность](#визуал-и-продуктивность)
		- [Finder](#finder)
		- [Dock](#dock)
			- [Настройки Dock](#настройки-dock)
		- [Оконный менеджмент](#оконный-менеджмент)
		- [Переключение между приложениями](#переключение-между-приложениями)
		- [Быстрый запуск](#быстрый-запуск)
		- [Остальные прилоежния, которые я использую ежедневно](#остальные-прилоежния-которые-я-использую-ежедневно)
	- [Кастомизация Menu Bar](#кастомизация-menu-bar)
		- [Bartender](#bartender)
	- [Python](#python)
			- [Pipenv](#pipenv)

## Системные настройки

Самое первое, что я делаю, это настраиваю мышку/клавиатуру для комфортного использования.

### Мышь
Здесь я ничего не меняю, только отключаю акселерацию мыши.
```
defaults write .GlobalPreferences com.apple.mouse.scaling -1
```

### Клавиатура

#### Клавиши
Меняю местами клавиши модицикации `control` и `command` т.к использую клавиатуру для Windows и мне так удобнее.

* Системные настроки -> Клавиатура -> Сочетания клавиш -> Клавиши модицикации
  * Клавиша Control - Command
  * Клавиша Command - Control

Тут же я добавляю бинд для открытия Launchpad.

* Системные настроки -> Клавиатура -> Сочетания клавиш -> Launchpad и Dock
  * Показывать Launchpad - Command + F4

Чтобы было удобнее переключать раскладку, устанавливаю [Punto Switcher с официального сайта](https://yandex.ru/soft/punto/mac/)

#### Ввод текста

По-умолчанию в источниках ввода стоит "Русский" и некоторые клавиши стоят "не на своих местах", поэтому меняем источник ввода на "Русский - ПК"

* Системные настроки -> Клавиатура -> Ввод текста -> Источники ввода -> Изменить -> + и добавляем "Русский - ПК"


## Homebrew / Terminal / Shell

### Homebrew

[Homebrew](https://brew.sh/) - это популярный пакетный менеджер для macOS. Он предоставляет простой способ установки приложений или инструментов с помощью командной строки.

Чтобы его установить, нужно открыть `Терминал` и вставить эту команду:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

После того, как установка Homebrew закончится, мы можем установить всё, что нам нужно.

### Terminal

Я не пользуюсь обычным терминалом, сразу меняю его на [iTerm2](https://iterm2.com/).
Его мы можем установить с помощью [Homebrew](#homebrew)
```
brew install iterm2
```
После установки, мы можем кастомизировать терминал как нам угодно. Мои настройки:

* Profile
  * Default
    * Text -> Font -> Monaco NF Mono
		* Скачать шрифт можно [здесь](https://github.com/Karmenzind/monaco-nerd-fonts).
  	* Text -> Font Size -> 14
  	* Window -> Transparency -> 20
  	* Window -> Blue -> 6
  	* Keys -> Key Mappings -> Presets -> Natural Text Editing

### Shell

По-умолчанию в качестве [Shell](https://en.wikipedia.org/wiki/Comparison_of_command_shells) в Mac используется `zsh`. Он мне нравится 🙂

#### Fig

[Fig](https://fig.io/) делает командную строку очень удобной. Самая популярная его вишка это Autocomplete. По мимо этого, он имеет поддержку скриптов, управлением серверами с помощью SSH, лёгкое редактирование Dotfiles и поддержку множества плагинов.

> Подробнее обо всём этом Вы можете посмотреть на их [сайте](https://fig.io/).


```
brew install fig
```

#### Плагины, которые использую
1. [You Should Use](https://app.fig.io/plugins/zsh-you-should-use_MichaelAquilina#configuration)
2. [Fast Syntax Highlight](https://app.fig.io/plugins/fast-syntax-highlighting_zdharma-continuum#configuration)
3. [Emoji CLI](https://app.fig.io/plugins/emoji-cli_b4b4r07#configuration)
4. [Zsh Autoswitch Python Virtualenv](https://app.fig.io/plugins/zsh-autoswitch-virtualenv_MichaelAquilina#configuration)
5. [Zsh Autosuggestions](https://app.fig.io/plugins/zsh-autosuggestions#configuration)
6. [Zsh Completions](https://app.fig.io/plugins/zsh-completions#configuration)
7. [256color Zsh](https://app.fig.io/plugins/zsh-256color_chrissicool#configuration)
8. [SpaceShip Prompt](https://app.fig.io/plugins/spaceship-prompt#configuration)
9. [Zsh History Substring Search](https://app.fig.io/plugins/zsh-history-substring-search#configuration)
10. [Oh my Zsh](https://app.fig.io/plugins/ohmyzsh#configuration)

#### Дополнения
Дополнительно использую `neofetch`, чтобы выводить информацию о системе в консоль, и `exa`, подробнее о [Exa](https://github.com/ogham/exa) можно узнать [тут](https://github.com/ogham/exa)

```
brew install neofetch
brew install exa
```

#### Git

Изначально Mac идёт с старой версией Git или его вообще нет. Чтобы проверить установлен ли Git нужно ввести:
```
git --version
```

Установим последнюю версию Git с помощью Homebrew:
```
brew install git
```

Настроим Git, чтобы мы могли его использовать под своим именем/почтой и настроим предпочтительный редактор.

```
git config --global user.name MAGICX
git config --global user.email haxgun@null.computer
git config --global core.editor nano
```

## Визуал и продуктивность

### Finder

* Finder -> Настройки
  * Основные -> Показывать на Рабочем столе-> Убираю галочки везде

	Стараюсь сохранять свой рабочий стол чистым.

  * Основные -> Показывать в новых окнах Finder -> Домашнюю папку

  * Дополнения -> Показывать все расширения имен файлов -> Да
  * Дополнения -> Предупреждать при изменении расширения -> Нет
  * Дополнения -> При выполнении поиска -> Искать в текущей папке

### Dock

По-умолчанию Dock засорён программами, которыми я не пользуюсь. Убираю всё и оставляю самое необходимое:

<details>
	<summary>Приложения</summary>
    1. Finder
    2. Arc Browser
    3. Telegram
    4. Discord
    5. VSCode
    6. Pycharm
    7. iTerm2
    8. Figma
    9. Spotify
    10. ColorPicker
    11. Postman
</details>

Также меняю иконки для эстетичности с помощью Pictogram
```
brew install pictogram
```
Иконки скачиваю с сайта [macicons.com](https://macosicons.com/#/)

![Dock](https://i.imgur.com/DVrt8PC.png)

#### Настройки Dock
Выключаю показывание недавних программ
* Настройки Dock -> Показать недавние программы в Dock

Меняю размер панели

![Настройки Dock](https://i.imgur.com/8jy4Ocn.png)

И включаю "Автоматически скрывать/показывать Dock"

* Настройки Dock -> Автоматически скрывать/показывать Dock


### Оконный менеджмент

Часто пользовался этой фитчей в Windows, но в Mac её по какой-то причине нет.

Чтобы это исправить, я устанавливаю [Rectangle](https://rectangleapp.com/). Достаточно бесплатной версии.

```
brew install rectangle
```

### Переключение между приложениями

Встроенный переключатель приложений отображает только значки приложений, причем только один значок на одно приложение, независимо от количества открытых в нем окон.

Я использую переключатель приложений под названием AltTab. Он показывает полный предварительный просмотр окон и имеет возможность показывать предварительный просмотр для каждого открытого окна во всех приложениях (даже свернутых).

Я заменяю встроенное сочетание клавиш CMD+TAB на AltTab.

```
brew install alt-tab
```

### Быстрый запуск

В Mac есть поисковик Spotlight, но он работает достаточно медленно и в основнов ищем запросы в интернете, а не папки и иногда промахивается и не находит нужные приложения.

Вместо него я использую [Reycast](https://www.raycast.com/), который имеет множество функций, по сравнению с Spotlight: впечатляющую скорость, встроенный калькулятор, конвертер, расширения и многое другое.

Советую ознакомиться с его функционалом на оф.сайте [Reycast](https://www.raycast.com/).

```
brew install raycast
```

### Остальные прилоежния, которые я использую ежедневно
* [Chrome](https://www.google.com/intl/ru_ru/chrome/) - браузер
* [Spotify](https://www.spotify.com/) - музыка
* [Telegram](https://telegram.org/) - месседжер
* [Discord](https://discord.com/) - месседжер / общение
* [Node.js](https://nodejs.org) - среда выполнения JavaScript
* [VSCode](https://code.visualstudio.com/) - редактор кода
* [Pycharm](https://www.jetbrains.com/ru-ru/pycharm/) - мощная IDE для Python
* [CleanShot X](https://cleanshot.com/) - скриншоты (платный)
* [MonitorControl](https://github.com/MonitorControl/MonitorControl) - настройка яркости монитора
* [AppCleaner](https://freemacsoft.net/appcleaner/) - при удалении приложения, будет искать файлы, оставленные приложением в системе, и настройки, которые должны быть удалены
* [KeepingYouAwake](https://keepingyouawake.app/) - недаёт уйти Mac'у в сон
* [Vlc](https://www.videolan.org/) - для просмотра фильмов / видео вместо QuickTime
* [Postman](https://www.postman.com/) - тестирование HTTP / REST / GraphQL запросов
* [WireGuard](https://www.wireguard.com/) - VPN
* [ColorPicker](https://apps.apple.com/ru/app/system-color-picker/id1545870783?mt=12) - удобное приложения для выбора цвета с экрана
* [OBS](https://obsproject.com/ru) - для стриминга на Twitch

Большинство этих приложений можно установить с помощью Homebrew:
```
google-chrome
spotify
telegram-desktop
discord
node
visual-studio-code
pycharm
cleanshot
monitorcontrol
appcleaner
keepingyouawake
vlc
postman
obs
```

```
xargs brew install < apps.txt
```

## Кастомизация Menu Bar

### Bartender

Мне не хочется видеть некоторые иконки на панеле, поэтому я их скрываю с помощью [Bartender](https://www.macbartender.com/).

Купить его можно на [официальном сайте](https://www.macbartender.com/).

## Python

Из коробки Mac имеет старую версию Python, мне необходима версия 3.11.4, поэтому я устанавливаю её.

Здесь я просто перехожу на официальный сайт, [скачиваю установщик](https://www.python.org/ftp/python/3.11.4/python-3.11.4-macos11.pkg) и устанавливаю с помощью него.

#### Pipenv
Дополнительно устанавливаю [pipenv](https://pipenv.pypa.io/en/latest/) для работы с виртуальными окружениями.

```
brew install pipenv
```
