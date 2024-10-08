# Практическая работа "Обнаружение фальшивых новостей"

Задача: используя библиотеку sklearn построить модель классического машинного обучения, которая может с высокой точностью более 90% определять, является ли новость реальной (REAL） или фальшивой（FAKE).

Для обучения был выбран датасет [fake_news.csv](https://storage.yandexcloud.net/academy.ai/practica/fake_news.csv)

В данном датасете количество реальных и фейковых новостей примерно равно:
![image](https://github.com/user-attachments/assets/3bce86bc-482e-4b08-a99b-9094963d40f3)

Наиболее часто встречающиеся слова в данном датасете для каждого из признаков (визуализировано с помощью библиотеки WorldCloud):
![image](https://github.com/user-attachments/assets/dd22d184-a861-4f5c-9bdf-f56cdf38f5b4)


Для решения задачи был использован классификатор PassiveAggressiveClassifier на векторных представлениях TF-IDF.
Результатом обучения стала модель с точностью 92.66%. Ниже представлена матрица ошибок для данной модели:
![image](https://github.com/user-attachments/assets/4c04fc56-2ac8-42e5-91f3-cf7ce1d640b1)

Код с решением задачи [Обнаружение_фальшивых_новостей.ipynb](https://github.com/awessine/fake_news_detection/blob/f86efa05cc0bee00dec6afdac851b1fef85e9c47/%D0%9E%D0%B1%D0%BD%D0%B0%D1%80%D1%83%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5_%D1%84%D0%B0%D0%BB%D1%8C%D1%88%D0%B8%D0%B2%D1%8B%D1%85_%D0%BD%D0%BE%D0%B2%D0%BE%D1%81%D1%82%D0%B5%D0%B9.ipynb)
