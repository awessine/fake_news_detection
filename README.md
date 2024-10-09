# Классификация фейковых новостей с использованием Passive Aggressive Classifier

Этот проект реализует классификацию новостей на основе их подлинности (реальные или фейковые) с использованием метода Passive Aggressive Classifier (PAC) из библиотеки scikit-learn. В проекте также используются библиотеки для обработки текста и визуализации, такие как NLTK, spaCy и WordCloud.
Для решения задачи был использован классификатор PassiveAggressiveClassifier на векторных представлениях TF-IDF.
Результатом обучения стала модель с точностью 92.66%. Ниже представлена матрица ошибок для данной модели:

![image](https://github.com/user-attachments/assets/4c04fc56-2ac8-42e5-91f3-cf7ce1d640b1)

## Установка

### Предварительные требования

Убедитесь, что у вас установлен Python версии 3.6 или выше. Вам также понадобятся следующие библиотеки:

```bash
pip install wordcloud
pip install nltk spacy
python -m spacy download en_core_web_sm
pip install numpy pandas matplotlib plotly scikit-learn
```
## Набор данных

Используемый в проекте набор данных — [fake_news.csv](https://storage.yandexcloud.net/academy.ai/practica/fake_news.csv), содержащий как реальные, так и фейковые новости, что позволяет проводить анализ и обучение моделей машинного обучения для классификации новостей по их подлинности.

#### Пример строк набора данных

| Unnamed: 0 | title                                           | text                                                                                                      | label |
|-------------|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------|
| 8476        | You Can Smell Hillary’s Fear                   | Daniel Greenfield, a Shillman Journalism Fellow at the David Horowitz Freedom Center.                     | FAKE  |
| 10294       | Watch The Exact Moment Paul Ryan Committed Pol..| Google Pinterest Digg LinkedIn Reddit StumbleUpon.                                                        | FAKE  |
| 3608        | Kerry to go to Paris in gesture of sympathy    | U.S. Secretary of State John F. Kerry said Monday.                                                        | REAL  |
| 10142       | Bernie supporters on Twitter erupt in anger ag..| — Kaydee King (@KaydeeKing) November 9, 2016 The.                                                         | FAKE  |
| 875         | The Battle of New York: Why This Primary Matters| It’s primary day in New York and front-runners are determined to win the coveted delegates.               | REAL  |

Соотношение реальных и фейковых новостей примерно равно:
![image](https://github.com/user-attachments/assets/3bce86bc-482e-4b08-a99b-9094963d40f3)

Наиболее часто встречающиеся слова в данном датасете для каждого из признаков (визуализировано с помощью библиотеки WorldCloud):
![image](https://github.com/user-attachments/assets/dd22d184-a861-4f5c-9bdf-f56cdf38f5b4)

## Пример вывода
```text
Точность: 95.20%
Clasification report:
              precision    recall  f1-score   support

       FAKE       0.95      0.95      0.95       104
       REAL       0.95      0.95      0.95       104

    accuracy                           0.95       208
   macro avg       0.95      0.95      0.95       208
weighted avg       0.95      0.95      0.95       208

```
