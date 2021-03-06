VkStatusPy - простой способ для работы со статусом в ВК!
--------------------------------------------------------

|VkStatusPy Logo|

**VkStatusPy** позволяет легче взаимодействовать со статусами во
ВКонтакте! VkStatusPy работает быстро и хорошо в своём деле!

Инструкция:
~~~~~~~~~~~

Установка модуля **VkStatusPy** с **pypi.org**:

    pip3 install VkStatusPy

Использование модуля:
~~~~~~~~~~~~~~~~~~~~~

Импортирование модуля **VkStatusPy**:

.. code:: py

    from VkStatusPy import *

Подключение вашего API-токена:

.. code:: py

    test = VkStatusPy(token="ВАШ_ТОКЕН")

Доступные методы:

.. code:: py

    test.set_status(text)
    test.set_status_group(text, group_id)
    test.get_status(user_id)
    test.get_status_group(group_id)

    # text - строка; user_id - положительное число; group_id - положительно число.

Получение статуса:

.. code:: py

    test.get_status(user_id=ID_ПОЛЬЗОВАТЕЛЯ)
    >> Текст статуса

    test.get_status_group(group_id=ID_ГРУППЫ)
    >> Текст статуса группы

Обновление статуса (установка своего значения):

.. code:: py


    # В случае успеха смены статуса, будет возвращаться значение - 1.

    test.set_status(text="ВАШ_ТЕКСТ")
    >> 1

    test.set_status_group(text="ВАШ_ТЕКСТ", group_id=ID_ГРУППЫ)
    >> 1

Возможные ошибки:

    **Error [15]** - доступ отклонен. Нету доступа к данной группе.

    **Error [100]** - неверное ID группы/полозователя.

    **Error [221]** - пользователя отключил трансляцию название музыки в
    статус.

.. |VkStatusPy Logo| image:: https://i.imgur.com/KicDzKe.png
