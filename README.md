# Introduction-to-the-processing-of-a-natural-language

## Курсовой проект по теме "Введение в обработку естественного языка"
Основная задача создание чат-бота в Telegram. Буду использовать датасеты с проекта "ответы mail.ru", а так же "youla.ru"
Бот умеет поболтать и предложить одежду с проекта Юла. 

Стек:

ML: FastText, CountVectorizer, TfidfVectorizer, MorphAnalyzer, LogisticRegression, annoy\
API: telegram


При поступлении текстового запроса модель сначала определяет является ли запрос на тему "поговорить" или "поиск продукта" с помощью MorphAnalyzer, CountVectorizer
и LogisticRegression. Если запрос продуктовый, то используя FastText, TfidfVectorizer и annoy определяются 3 наиболее подходящие продукта, которые затем отображаются
в чате. Если же запрос разговорный, то используя те же FastText, TfidfVectorizer и annoy определяется наиболее подходящий ответ.
