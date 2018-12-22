# Робо-журналистика. Мини-проект

## Программа для подбора изображений к тексту

Пользователь загружает англоязычный текст и получает файл с ключевыми словами и ссылками на 30 (макисмум) изображений к тексту с сервиса Flickr, которые можно использовать в коммерческих целях без указания авторства (No known copyright restrictions, Public Domain Dedication (CC0), Public Domain Mark). В файле содержится также название изображения и 2 ссылки на него: большой и средний размер.

### Алгоритм

1. Программа принимает на вход файл с англоязычным текстом в формате txt
2. Обработка текста
    + Все слова с маленькой буквы, без знаков препинания
    + Подсчитывается частота каждого слова (Counter)
    + Поиск стоп-слов в тексте (файл "stop-list.txt") и присвоение стоп-словам частоты равной 0
    + Выделение 5 ключевых слов текста
3. Запрос к API Flickr (задается список тегов, поиск изображений со свободной лицензией)
4. Выбор необходимых данных: title, farm, id, server, secret
5. Формирование ссылок на фото
6. Запись необходимых данных в файл "links_to_images.txt": ключевые слова, порядковый номер, название фото, ссылки

JPhoto_AYNesterov.ipynb – код программы
journ.txt – пример текста (источник: https://www.psychologytoday.com/us/blog/darwins-subterranean-world/201812/do-dogs-engage-in-lucid-dreaming)
links_to_images.txt – результат

<b><i>Андрей Нестеров, МДЖ172</i></b>
