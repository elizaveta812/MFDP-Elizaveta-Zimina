1.  Бизнес-анализ (Business Understanding)

*Организационная структура:* Основные пользователи - люди, желающие следить за здоровьем своего сердца. Те, у кого уже есть история сердечных заболеваний, или те, кто находится в группе риска

*Какова бизнес-цель проекта?* Мониторинг состояния сердца и своевременное оповещение об анормальной частоте сердечных сокращений

*Существуют ли какие-то уже разработанные решения? Если существуют, то какие и чем именно текущее решение не устраивает?* Умные часы и фитнес браслеты на данный момент хорошо справляются с задачей отслеживания физиологических показателей человека, а также удобны для напоминаний и оповещений. Например, могут напоминать, что нужно пить больше воды или выполнять норму по количеству пройденных шагов. Однако тем, кто переживает о состоянии своего сердца, важно, чтобы показатели не просто отслеживались, а анализировались. Важно также замечать все аномалии и своевременно оповещать пользователя, что и является нашей задачей. 

1.1 Текущая ситуация (Assessing current solution)

*Есть ли доступное железо или его необходимо закупать?* Есть, дополнительно закупать ничего не потребуется

*Где и как хранятся данные, будет ли предоставлен доступ в эти системы, нужно ли дополнительно докупать/собирать внешние данные?* Дополнительно докупать данные не придется - всё есть в публичном доступе, однако возможно понадобится повторный сбор данных, если основной датасет не покроет все нужды. Данные будут храниться в облачном хранилище MinIO. На текущий момент основной датасет - https://www.kaggle.com/datasets/kekosingh/smart-watch-health-analysis

*Вероятные риски проекта*

В основном риски связаны с данными:
 1) Малое количество данных, которые не позволят получить эффективную модель.
 2) Данные качественные, но среди них не будет анормальных показателей, необходимых для выявления целевой переменной.

1.2 Решаемые задачи с точки зрения аналитики (Data Mining goals)

*Какую метрику мы будем использовать?* F-мера (или Precision / Recall)

*Каков критерий успешности модели?*  Для начала возьмем стандартный порог 0.5 и в процессе работы с данными скорректируем его

1.3 План проекта (Project Plan)
Как только получены ответы на все основные вопросы и ясна цель проекта, время составить план проекта. План должен
содержать оценку всех шести фаз внедрения.
