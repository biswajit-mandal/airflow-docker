Start airflow service by
`make up`

To create a fernet key (AIRFLOW__CORE__FERNET_KEY) required in .env file:
```
from cryptography.fernet import Fernet
fernet_key = Fernet.generate_key()
print(fernet_key.decode())
```

To navigate airflow UI:
```
http://<IP>:8080/
```
Default user-id/password for login is: `airflow`/`airflow`

To run the airflow cli commands:
`docker-compose run airflow-cli <command>`
For example:

```
docker-compose run airflow-cli airflow dags list
```
