# ML_docker_flask_project
course project (GB ML in business)

Итоговый проект курса "Машинное обучение в бизнесе"

Стек:

ML: sklearn, pandas, numpy
API: flask
Данные: с kaggle - https://www.kaggle.com/barun2104/telecom-churn

Задача: предсказать отток клиентов (поле churn). Бинарная классификация


Используемые признаки:

AccountWeeks - number of weeks customer has had active account

ContractRenewal - 1 if customer recently renewed contract, 0 if not

DataPlan - 1 if customer has data plan, 0 if not

DataUsage - gigabytes of monthly data usage

CustServCalls - number of calls into customer service

DayMins - average daytime minutes per month

DayCalls - average number of daytime calls

MonthlyCharge - average monthly bill

OverageFee - largest overage fee in last 12 months

RoamMins - average number of roaming minutes

Преобразования признаков: StandardScaler, OHEEncoder

Модель: RandomForest

git@github.com:SLVmain/ML_docker_flask_project.git
### Клонируем репозиторий и создаем образ
```
$ git clone https://github.com/SLVmain/ML_docker_flask_project.git
$ cd ML_docker_flask_project
$ docker build -t ml_docker_flask_project .
```

### Запускаем контейнер


Здесь Вам нужно создать каталог локально и сохранить туда предобученную модель (<your_local_path_to_pretrained_models> нужно заменить на полный путь к этому каталогу)
```
$ docker run -d -p 8180:8180 -v <your_local_path_to_pretrained_models>:/app/app/models ml_docker_flask_project
```

### Переходим на localhost:8180

#/Users/Skytandem/GEEKBRAINS/Машинное обучение в бизнесе/Машинное обученгие 2/project/randomforest_pipeline.dill
