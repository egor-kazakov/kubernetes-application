# Helm-Chart
## Описание
Helm-chart с приложением на Flask. 

Deployment:
* Flask
* Redis c pvc запросом

Сервисы:
* service flask - для работы ingress
* service redis - для обращения к БД

Ingress:
* flask.s<номер вашего логина>.edu.slurm.io с выпуском TLS-сертификата с помощью Cert-manager

## Переменные
| Переменная | Описание |
|----------|-------------|
| image.repository | путь к репозиторию |
| tag | версия образа |
| imagePullSecret | токен реестра |
| replicas | количество реплик |
| resources | лимиты и реквесты пода flask |
| service.app_port | порт приложения flask |
| service.port | порт ingress |
| ingress.host | алрес ingress |
