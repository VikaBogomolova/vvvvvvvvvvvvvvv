Отчет по интеграции логгера в приложение на Tkinter

1.Описание экосистемы

Приложение представляет собой простое графическое приложение на Tkinter, которое генерирует лог-сообщение и отображает его в всплывающем окне.

2.Выбранный логгер: logging

logging - это встроенный модуль в Python, предоставляющий стандартный API для логирования, позволяющий гибко настроить обработку логов.

3.Обоснование выбора

Выбор logging обусловлен следующими факторами:

Встроенный модуль: Не требуется установки дополнительных библиотек.
Гибкость:  logging позволяет легко настроить уровни логгирования, форматы сообщений и обработчики логов.
Стандартный API:  Стандартный модуль Python,  широко используется в сообществе разработчиков.

4. Реализация

1. Настройка логгера:
import logging

5.Настройка логирования
logging.basicConfig(level=logging.DEBUG, format='%(asctime)s - %(levelname)s - %(message)s')

В этой части кода мы используем logging.basicConfig для настройки основного логгера. Устанавливаем уровень логгирования на logging.DEBUG, чтобы записывались все сообщения, включая отладочные. Формат сообщения также настраивается.

2. Создание функции для логирования:
def log_message():
     Генерируем лог-сообщение
    message = "Это сообщение лога."
    logging.debug(message)
    
     Отображаем сообщение в всплывающем окне
    messagebox.showinfo("Лог-сообщение", message)

В этой функции log_message мы генерируем лог-сообщение и записываем его в лог с помощью logging.debug(message). Затем мы отображаем сообщение в всплывающем окне с помощью messagebox.showinfo.

3. Создание графического интерфейса:
import tkinter as tk
from tkinter import messagebox

 ... (код для логирования) ...

 Создание основного окна
root = tk.Tk()
root.title("Логгирование в окошке")

 Создание кнопки для логирования
log_button = tk.Button(root, text="Сгенерировать лог", command=log_message)
log_button.pack(pady=20)

 Запуск главного цикла приложения
root.mainloop()

В этой части кода мы создаем основное окно Tkinter, кнопку "Сгенерировать лог", которая вызывает функцию log_message при нажатии.

6. Результаты

![image](https://github.com/user-attachments/assets/331222cd-8a6c-4033-8401-81d68ab86f93)


![image](https://github.com/user-attachments/assets/3312d163-6d9b-42d1-9c68-93af10d99c3b)
![image](https://github.com/user-attachments/assets/04f33faf-6931-48ce-b09f-86ff6b38dcb7)
![image](https://github.com/user-attachments/assets/3dde1a4c-b026-4af7-a04e-3d0fd21bba11)


При нажатии на кнопку "Сгенерировать лог" в консоли выводится лог-сообщение с меткой времени, уровнем и самим сообщением. Также появляется всплывающее окно с тем же сообщением.

7.Выводы

Интеграция логгера logging в приложение на Tkinter позволяет удобно записывать логи и отображать их в консоли, а также в графическом интерфейсе приложения.

 8.Дополнительные возможности

Настройка формата логов:  Можно настроить формат сообщений, добавляя метки, идентификаторы запросов и другую информацию.
Поддержка различных обработчиков: logging позволяет использовать различные обработчики,  отправляя логи в файлы, базы данных и другие системы.
Управление уровнями логгирования:  Можно изменять уровень логгирования во время выполнения приложения, чтобы управлять количеством собираемых данных. 
Запись логов в файл: Можно использовать logging.FileHandler для записи логов в файл вместо консоли.
