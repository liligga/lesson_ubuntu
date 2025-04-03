---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Welcome to Slidev
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev
---

# Операционные Системы

---

## Что такое Операционная Система (ОС)?

<br>

ОС - это **"мозг"** компьютера.

<ul>
  <li class="text-xl">Управляет всем "железом" (CPU, память, диски).</li>
  <li class="text-xl">Предоставляет "сцену" для запуска программ (браузер, игры).</li>
  <li class="text-xl">Посредник между <span v-mark.red>программами</span> и <span v-mark.blue>оборудованием</span>.</li>
</ul>



---

## Примеры Операционных Систем

<div class="grid grid-cols-3 gap-4 pt-10">
  <div>
    <p class="text-center mt-2"><strong>Windows</strong></p>
    <p class="text-sm text-center">Самая популярная ОС для домашних ПК и игр.<br>(Microsoft: Билл Гейтс, Пол Аллен)</p>
  </div>
  <div>
    <p class="text-center mt-2"><strong>macOS</strong></p>
    <p class="text-sm text-center">ОС для компьютеров Apple. Известна дизайном.<br>(Apple: Стив Джобс, Стив Возняк)</p>
  </div>
  <div>
    <p class="text-center mt-2"><strong>Linux (ядро)</strong></p>
    <p class="text-sm text-center">Свободное ядро, основа многих ОС.<br>(Линус Торвальдс)</p>
  </div>
</div>

---

## Linux: Ядро ≠ Дистрибутив

<br>

Часто говорят "ОС Linux", но **Linux** - это *только ядро*.

<br>

**Ядро Linux** - основа, управляющая железом.

**Дистрибутив Linux** - полноценная ОС:
<ul>
  <li>✅ Ядро Linux</li>
  <li>✅ Системные утилиты (GNU и др.)</li>
  <li>✅ Графическая оболочка (GNOME, KDE...)</li>
  <li>✅ Прикладные программы</li>
</ul>

<br>
**Аналогия:** 
<ul>
  <li><span v-mark.brown>Ядро Linux</span> = Вафельный рожок (основа, ядро Linux)</li>
  <li><span v-mark.pink>Дистрибутив</span> = Мороженое (Ubuntu, Fedora...) + Посыпка (программы)</li>
</ul>

---

## Популярные Дистрибутивы Linux

<div class="grid grid-cols-3 gap-4 pt-4">
  <div>
    <p class="text-center mt-1"><strong>Ubuntu</strong></p>
    <p class="text-xs text-center">Дружелюбный к новичкам, большая поддержка.</p>
  </div>
  <div>
    <p class="text-center mt-1"><strong>Fedora</strong></p>
    <p class="text-xs text-center">Современный, новейшие технологии.</p>
  </div>
  <div>
    <p class="text-center mt-1"><strong>Debian</strong></p>
    <p class="text-xs text-center">Стабильный, основа для многих дистрибутивов.</p>
  </div>
  <div>
    <p class="text-center mt-1"><strong>Arch Linux</strong></p>
    <p class="text-xs text-center">Для опытных, гибкость, "сделай сам".</p>
  </div>
  <div>
    <p class="text-center mt-1"><strong>Linux Mint</strong></p>
    <p class="text-xs text-center">На базе Ubuntu, удобство "из коробки".</p>
  </div>
  <div>
    <p class="text-center mt-1"><strong>CentOS / RHEL</strong></p>
    <p class="text-xs text-center">Стабильность для серверов (Red Hat).</p>
  </div>
  <div>
    <p class="text-center mt-1"><strong>Pop!_OS</strong></p>
    <p class="text-xs text-center">На базе Ubuntu, оптимизирован для разработчиков и геймеров.</p>
  </div>
  <div>
    <p class="text-center mt-1"><strong>SteamOS</strong></p>
    <p class="text-xs text-center">От Valve, оптимизирован для игр, основа Steam Deck.</p>
  </div>
</div>

---
layout: center
class: text-center
---

# Основы Работы в Терминале

---

## Знакомство с Терминалом

<br>

Терминал (командная строка, shell, консоль) - это **текстовый интерфейс** для взаимодействия с ОС.

<ul>
  <li>Вместо кликов мышкой - <span v-mark>текстовые команды</span>.</li>
  <li>Мощный инструмент для разработчиков и администраторов.</li>
  <li>Позволяет автоматизировать задачи.</li>
</ul>

<br>
<img src="https://miro.medium.com/v2/resize:fit:1400/1*LSYeXUI8g7DY7B9paRPfkw.png" class="h-45 mx-auto" alt="Пример терминала"/>

---

## Базовые Команды: Навигация

<v-clicks>

*   `pwd` (print working directory): Показать <span v-mark>текущую папку</span>.
    ```bash
    $ pwd
    /home/user/projects
    ```
*   `ls` (list): Показать <span v-mark>содержимое папки</span>.
    ```bash
    $ ls
    file1.txt  documents  script.sh
    ```
    *   `ls -l`: Подробный вид
    *   `ls -a`: Показать скрытые файлы (`.bashrc`)
    *   `ls -h`: Показать размеры файлов
*   `cd` (change directory): <span v-mark>Перейти</span> в другую папку.
    ```bash
    $ cd documents  # В папку documents
    $ cd ..         # На уровень выше
    $ cd ~          # В домашнюю папку (/home/user)
    $ cd            # То же, что cd ~
    ```

</v-clicks>

---

## Базовые Команды: Файлы и Папки (1)

<v-clicks>

*   `mkdir` (make directory): <span v-mark>Создать папку</span>.
    ```bash
    $ mkdir my_new_folder
    $ ls
    documents  file1.txt  my_new_folder  script.sh
    $ mkdir -p folder1/folder2
    ```
    *   `-p` - Создает родительские папки, если они не существуют
    * Важно: Желательно создавать папки и файлы без пробелов!!
*   `touch`: <span v-mark>Создать пустой файл</span> (или обновить время доступа).
    ```bash
    $ touch report.txt
    $ ls
    documents  file1.txt  my_new_folder  report.txt  script.sh
    ```
*   `cp` (copy): <span v-mark>Скопировать</span> файлы или папки.
    ```bash
    # Копировать файл
    $ cp report.txt report_backup.txt

    # Копировать папку (нужен ключ -r для рекурсии)
    $ cp -r documents documents_backup
    ```

</v-clicks>

---

## Базовые Команды: Файлы и Папки (2)

<v-clicks>

*   `mv` (move): <span v-mark>Переместить</span> или <span v-mark>переименовать</span>.
    ```bash
    # Переименовать файл
    $ mv report.txt final_report.txt

    # Переместить файл в папку
    $ mv final_report.txt my_new_folder/
    ```
*   `rm` (remove): <span v-mark.red>Удалить файлы</span>. **ОСТОРОЖНО! Нет корзины!**
    ```bash
    $ rm report_backup.txt
    ```
*   `rmdir` (remove directory): <span v-mark.orange>Удалить ПУСТУЮ папку</span>.
    ```bash
    $ rmdir old_empty_folder
    ```
*   `rm -r`: <span v-mark.red>Удалить папку СО ВСЕМ СОДЕРЖИМЫМ</span>. **ОЧЕНЬ ОСТОРОЖНО!**
    ```bash
    $ rm -r documents_backup
    ```

</v-clicks>

---

## Базовые Команды: Просмотр и Вывод

<v-clicks>

*   `cat` (concatenate): Показать содержимое файла <span v-mark>целиком</span>.
    ```bash
    $ cat final_report.txt
    Это содержимое файла отчета.
    ```
*   `less` / `more`: <span v-mark>Постраничный просмотр</span> больших файлов (выход - `q`).
    ```bash
    $ less /var/log/syslog
    ```
*   `head` / `tail`: Показать <span v-mark>начало</span> / <span v-mark>конец</span> файла.
    ```bash
    $ head -n 5 script.sh  # Первые 5 строк
    $ tail -n 10 script.sh # Последние 10 строк
    $ tail -f /var/log/syslog # Следить за файлом (логи)
    ```
*   `echo`: <span v-mark>Вывести текст</span> на экран.
    ```bash
    $ echo "Привет, Терминал!"
    Привет, Терминал!
    ```

</v-clicks>

---

## Базовые Команды: Помощь и Поиск

<v-clicks>

*   `man` (manual): Показать <span v-mark>инструкцию (руководство)</span> для команды.
    ```bash
    $ man ls
    # (Навигация стрелками, выход - q)
    ```
*   `--help`: Краткая справка от самой команды.
    ```bash
    $ ls --help
    $ cp --help
    ```
*   `grep`: <span v-mark>Поиск текста</span> внутри файлов.
    ```bash
    # Найти слово "Error" в лог-файле
    $ grep "Error" /var/log/syslog

    # Рекурсивный поиск (-r) без учета регистра (-i) в папке src
    $ grep -ri "function" ./src
    ```
</v-clicks>

---

## Базовые Команды: Система и Сеть (1)

<v-clicks>

*   `sudo` (superuser do): Выполнить команду <span v-mark>с правами администратора</span>. Часто требуется для установки/удаления ПО и системных настроек.
    ```bash
    # Обновить список пакетов и установить редактор nano (Debian/Ubuntu)
    $ sudo apt update && sudo apt install nano
    ```
*   `apt` (Advanced Package Tool): <span v-mark>Менеджер пакетов</span> в Debian/Ubuntu и их производных.
    ```bash
    # Найти пакет
    $ apt search screenfetch
    # Установить пакет
    $ sudo apt install screenfetch
    # Удалить пакет
    $ sudo apt remove screenfetch
    # Обновить список пакетов (перед установкой/обновлением)
    $ sudo apt update
    # Обновить установленные пакеты
    $ sudo apt upgrade
    ```
</v-clicks>

---

## Базовые Команды: Система и Сеть (2)

<v-clicks>

*   `snap`: <span v-mark>Универсальный менеджер пакетов</span>. Пакеты (`snap`-ы) содержат все зависимости.
    ```bash
    # Найти snap-пакет
    $ snap find spotify
    # Установить snap-пакет
    $ sudo snap install spotify
    # Удалить snap-пакет
    $ sudo snap remove spotify
    # Обновить все snap-пакеты
    $ sudo snap refresh
    # Показать список установленных snap-пакетов
    $ snap list
    ```
*   `ping`: <span v-mark>Проверить доступность</span> хоста в сети.
    ```bash
    $ ping google.com
    # (Остановить - Ctrl+C)
    $ ping -c 4 8.8.8.8
    ```
</v-clicks>

---

## Базовые Команды: Поиск и Управление 

<v-clicks>

*   `find`: <span v-mark>Поиск файлов</span> по разным критериям.
    ```bash
    # Найти все .log файлы в /var/log
    $ find /var/log -name "*.log"

    # Найти файлы больше 100 МБ в домашней папке
    $ find ~ -size +100M

    # Найти папки с именем 'temp' в текущей директории
    $ find . -type d -name "temp"
    ```
*   `tar` (tape archive): Работа с архивами. <span v-mark>Извлечение из `.tar.gz`</span>.
    ```bash
    # Распаковать архив app.tar.gz в текущую папку
    $ tar -xzvf app.tar.gz
    # x: извлечь, z: использовать gzip, v: подробно, f: из файла

    # Создать архив my_files.tar.gz из папки documents
    $ tar -czvf my_files.tar.gz ./documents
    # c: создать, z: gzip, v: подробно, f: в файл
    ```
</v-clicks>

---

## Базовые Команды: Управление Системой

<v-clicks>

*   `reboot`: <span v-mark.orange>Перезагрузить систему</span>. (Требует `sudo`)
    ```bash
    $ sudo reboot
    ```
*   `shutdown`: <span v-mark.red>Выключить систему</span>. (Требует `sudo`)
    ```bash
    # Выключить немедленно
    $ sudo shutdown now

    # Отменить запланированное выключение
    $ sudo shutdown -c

    # Выключить через 15 минут с сообщением
    $ sudo shutdown +15 "Система будет выключена через 15 минут."
    ```
</v-clicks>

---

## Базовые Команды: Разное

<v-clicks>

*   `clear`: <span v-mark>Очистить</span> экран терминала.
*   `history`: Показать <span v-mark>историю команд</span>.
*   `exit`: <span v-mark>Завершить</span> сессию терминала.
<br>

**Полезные сочетания клавиш:**
*   <kbd>Ctrl</kbd> + <kbd>C</kbd>: <span v-mark.red>Прервать</span> текущую команду.
*   <kbd>Ctrl</kbd> + <kbd>D</kbd>: Сигнал конца ввода (часто = `exit`).
*   <kbd>Tab</kbd>: <span v-mark.green>Автодополнение</span> команд и путей (используйте постоянно!).
*   <kbd>↑</kbd> / <kbd>↓</kbd>: Навигация по истории команд.
*   <kbd>Ctrl</kbd> + <kbd>B</kbd>: Показать/Скрыть боковую панель (Explorer).
*   <kbd>Alt</kbd> + <kbd>Tab</kbd>: Переключение между открытыми файлами.
</v-clicks>

---
layout: center
class: text-center
---

# Практика - лучший учитель!

Пробуйте команды в своем терминале.

---

## VS Code: Основные Горячие Клавиши (1)

<div class="grid grid-cols-2 gap-4">
<div>

**Общие**
<ul>
<li><kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> / <kbd>F1</kbd>: Палитра команд</li>
<li><kbd>Ctrl</kbd>+<kbd>P</kbd>: Быстрый переход к файлу</li>
<li><kbd>Ctrl</kbd>+<kbd>,</kbd>: Настройки</li>
<li><kbd>Ctrl</kbd>+<kbd>K</kbd> <kbd>Ctrl</kbd>+<kbd>S</kbd>: Список горячих клавиш</li>
<li><kbd>Ctrl</kbd>+<kbd>`</kbd>: Открыть/Закрыть встроенный терминал</li>
</ul>
</div>
<div>

  **Редактирование**
<ul>
<li><kbd>Ctrl</kbd>+<kbd>X</kbd>: Вырезать строку (без выделения)</li>
<li><kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>K</kbd>: Удалить строку (не вырезать)</li>
<li><kbd>Ctrl</kbd>+<kbd>C</kbd>: Копировать строку (без выделения)</li>
<li><kbd>Alt</kbd>+<kbd>↑</kbd>/<kbd>↓</kbd>: Переместить строку вверх/вниз</li>
<li><kbd>Shift</kbd>+<kbd>Alt</kbd>+<kbd>↑</kbd>/<kbd>↓</kbd>: Дублировать строку вверх/вниз</li>
<li><kbd>Ctrl</kbd>+<kbd>/</kbd>: Закомментировать/Раскомментировать строку или блок</li>
<li><kbd>Ctrl</kbd>+<kbd>Enter</kbd>: Вставить строку ниже</li>
<li><kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>Enter</kbd>: Вставить строку выше</li>
</ul>
</div>
</div>

---

## VS Code: Основные Горячие Клавиши (2)

<div class="grid grid-cols-2 gap-4">
<div>

**Навигация**
<ul>
<li><kbd>Ctrl</kbd>+<kbd>Home</kbd>/<kbd>End</kbd>: В начало/конец файла</li>
<li><kbd>Home</kbd>/<kbd>End</kbd>: В начало/конец строки</li>
<li><kbd>Ctrl</kbd>+<kbd>G</kbd>: Перейти к строке</li>
<li><kbd>Ctrl</kbd>+<kbd>B</kbd>: Показать/Скрыть боковую панель (Explorer)</li>
<li><kbd>Ctrl</kbd>+<kbd>Tab</kbd>: Переключение между открытыми файлами</li>
</ul>
</div>
<div>

**Поиск и Замена**
<ul>
<li><kbd>Ctrl</kbd>+<kbd>F</kbd>: Найти в текущем файле</li>
<li><kbd>Ctrl</kbd>+<kbd>H</kbd>: Заменить в текущем файле</li>
<li><kbd>F3</kbd> / <kbd>Shift</kbd>+<kbd>F3</kbd>: Найти следующее/предыдущее совпадение</li>
<li><kbd>Alt</kbd>+<kbd>Enter</kbd>: Выделить все найденные совпадения</li>
<li><kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>F</kbd>: Поиск по всем файлам проекта</li>
<li><kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>H</kbd>: Замена по всем файлам проекта</li>
</ul>
</div>
</div>

---

## VS Code: Основные Горячие Клавиши (3)

<div class="grid grid-cols-2 gap-4">
<div>

**Мульти-курсор и Выделение**
<ul>
<li><kbd>Alt</kbd>+<kbd>Click</kbd>: Добавить курсор в место клика</li>
<li><kbd>Ctrl</kbd>+<kbd>D</kbd>: Выделить следующее слово, идентичное текущему</li>
<li><kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>L</kbd>: Выделить все вхождения текущего выделения</li>
<li><kbd>Shift</kbd>+<kbd>Alt</kbd>+<kbd>I</kbd>: Добавить курсоры в конец каждой выделенной строки</li>
</ul>
</div>
<div>

**Окна и Макет**
<ul>
<li><kbd>Ctrl</kbd>+<kbd>\</kbd>: Разделить редактор</li>
<li><kbd>Ctrl</kbd>+<kbd>1</kbd>/<kbd>2</kbd>/<kbd>3</kbd>: Фокус на 1/2/3 группу редакторов</li>
<li><kbd>Ctrl</kbd>+<kbd>W</kbd>: Закрыть текущий файл</li>
<li><kbd>Ctrl</kbd>+<kbd>K</kbd> <kbd>W</kbd>: Закрыть все файлы</li>
</ul>
</div>
</div>
