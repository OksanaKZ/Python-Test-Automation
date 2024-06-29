### В этом репозитории хранится теория и выполненные задания из курса "Автоматизация тестирования с помощью Selenium и Python" (stepik.org).  

---

Selenium – это проект, в рамках которого разрабатывается серия программных продуктов с открытым исходным кодом (open source):  
Selenium WebDriver,  
Selenium RC,  
Selenium Server,  
Selenium Grid,  
Selenium IDE...  

Selenium WebDriver, или просто WebDriver – это драйвер браузера, то есть не имеющая пользовательского интерфейса программная библиотека, которая позволяет различным другим программам взаимодействовать с браузером, управлять его поведением, получать от браузера какие-то данные и заставлять браузер выполнять какие-то команды. По сути своей это — универсальный интерфейс, который позволяет манипулировать разными браузерами напрямую из кода на языке программирования.

<img src="https://github.com/OksanaKZ/Python-Auto-Tests/blob/main/images/Selenium%20WebDriver.png"/>

WebDriver не имеет прямого отношения к тестированию. Он всего лишь предоставляет автотестам доступ к браузеру. Структурирование, группировку и запуск тестов, а также генерацию отчётов о тестировании, обеспечивает фреймворк тестирования, такой как JUnit или TestNG для Java, NUnit или Gallio для .Net, RSpec или Cucumber для Ruby и так далее. Разработка тестов ведётся в среде Eclipse, Intellij IDEA, Visual Studio, RubyMine и так далее. Сборка осуществляется посредством Maven, Gradle, Ant, NAnt,Rake и так далее. Запуск тестов по расписанию и публикацию отчётов выполняет сервер непрерывной интеграции – Jenkins, CruiseControl, Bamboo, TeamCity и так далее. И всё это – самостоятельные инструменты, не имеющие отношения к проекту Selenium.  

---
<details>
<summary>Инструкция для запуска браузера с помощью Selenium WebDriver</summary>

1. Установить Python3 ([официальный сайт](https://www.python.org/downloads/)). Во время установки поставить галочку в разделе Add Python 3.x to PATH (тогда вызов интерпретатора Python будет доступен из командной строки).
2. Создать виртуальное окружение (легко удалить или изменить). Все пакеты для Python, которые будут установлены позднее, будут доступны только в этом виртуальном окружении:
```
mkdir environments
cd environments
python -m venv selenium_env
```
3. Активировать виртуальное окружение:  
```
selenium_env\Scripts\activate.bat
```
4. В виртуальном окружении установить библиотеку Selenium:
```
pip install selenium==4.*
```
5. В виртуальном окружении установить PyTest:
```
pip install pytest==7.1.2
```
6. Cохранить все версии пакетов в специальный файл requirements.txt:
```
pip freeze > requirements.txt
```
Чтобы добавить все пакеты из файла в новом виртуальном окружении, ввести команду:  
```
pip install -r requirements.txt
```
7. Установить драйвер для браузера:  
- для Chrome скачать нужную версию драйвера ChromeDriver можно по [ссылке](https://googlechromelabs.github.io/chrome-for-testing/);
- создать на диске C: папку chromedriver и положите разархивированный ранее файл chromedriver.exe в папку C:\chromedriver;
- добавить в системную переменную PATH папку C:\chromedriver ([инструкция](https://www.computerhope.com/issues/ch000549.htm)).  
8. Для запуска интерпретатора Python ввести команду python.  
9. Деактивировать виртуальное окружение:  
```
deactivate.bat
```
</details>
