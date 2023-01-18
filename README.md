# Проект YaMDb


## Описание

Проект YaMDb собирает отзывы пользователей на произведения. Сами произведения в YaMDb не хранятся, здесь нельзя посмотреть фильм или послушать музыку.
Произведения делятся на категории, такие как «Книги», «Фильмы», «Музыка». Например, в категории «Книги» могут быть произведения «Винни-Пух и все-все-все» и «Марсианские хроники», а в категории «Музыка» — песня «Давеча» группы «Жуки» и вторая сюита Баха. Список категорий может быть расширен (например, можно добавить категорию «Изобразительное искусство» или «Ювелирка»).
Произведению может быть присвоен жанр из списка предустановленных (например, «Сказка», «Рок» или «Артхаус»).
Добавлять произведения, категории и жанры может только администратор.
Благодарные или возмущённые пользователи оставляют к произведениям текстовые отзывы и ставят произведению оценку в диапазоне от одного до десяти (целое число); из пользовательских оценок формируется усреднённая оценка произведения — рейтинг (целое число). На одно произведение пользователь может оставить только один отзыв.
Добавлять отзывы, комментарии и ставить оценки могут только аутентифицированные пользователи.


## Развертывание контейнера

> Предварительно у вас должны быть установлены Docker и Docker-compose

- Перейти в папку infra/;
- Выполнить команду по развертыванию контейнера:
```sudo docker-compose up```
- Выполнить миграции:
```sudo docker-compose exec web python manage.py migrate```
- Создайте пользователя-админастратора:
```sudo docker-compose exec web python manage.py createsuperuser```
- Заполните базу данных данными следующей командой:
```sudo docker-compose exec web python manage.py loaddata fixtures.json```
- Теперь проект доступен в вашем браузере по адресу localhost.


## Технологии:

- Python 3.7
- Django 2.2
- Django REST Framework
- JWT
- Docker
- Docker-compose


## Над проектом трудились:

- Наташа Сорокина
- Евгений Балуев
- Юрий Троянов

## В контенер паковал:

- Юрий Троянов
