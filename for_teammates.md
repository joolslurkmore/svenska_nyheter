## Работа в терминале Powershell, настройка на локальном компьютере Windows 
Установка последней версиии языка, подключение Github

```
winget search python 
winget install --id Python.Python.3.13 -e  #выбрать самый новый питон 13. опция -e (или --exact) находит Id

python --version # проверка установки
pip --version

winget install --id Git.Git -e # github установка

# перезапуск терминала

git --version #проверка версии

```
### Настройка среды выполнения в Visual Studio code, 
Установка виртуальной среды для логичной работы с библиотеками (делаем в терминале вс кода)
создаём виртуальное окружение с помощью Python 3.13, создаст папку .venv в корне проекта

```
py -3.13 -m venv .venv

Set-ExecutionPolicy -Scope CurrentUser RemoteSigned #для запуска скриптов

.\.venv\Scripts\Activate.ps1
Установка основных библиотек для работы
pip install python-telegram-bot requests beautifulsoup4 deepseek googletrans==4.0.0-rc1 nltk python-dotenv

pip freeze > requirements.txt #сохраним в отдельный файл настройки среды

git init #инициаилизация
git add .


```

`python-telegram-bot` для работы с Telegram API

`requests` и `beautifulsoup4` для парсинга сайтов

`deepseek` для GPT

`googletrans` для переводов

`nltk` для синонимов

`python-dotenv` для загрузки .env
