

```shell
git clone git@github.com:244Walyson/Kanban-backend.git
cd Kanban-backend
docker build -t kanban-backend .
docker run --name kanban -p 8080:8081 kanban-backend
````
**se quiser rode a branch auth e a que tem login e controlle de acesso, time, board e outros trem la acesse o swagger para ver os endpoints [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)**

```shell
git clone git@github.com:244Walyson/Kanban-backend.git
cd Kanban-backend
git checkout auth
docker build -t kanban-backend .
docker run --name kanban -p 8080:8081 kanban-backend
````
## login
```shell
http://localhost:8080/oauth2/token
```
## curl
```curl
curl --location --globoff 'http://localhost:8080/oauth2/token' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--header 'Authorization: Basic bXljbGllbnRpZDpteWNsaWVudHNlY3JldA==' \
--data-urlencode 'username=maria@gmail.com' \
--data-urlencode 'password=123456' \
--data-urlencode 'grant_type=password'
```
### usuario test: 
username: 
```plaintext 
maria@gmail.com
```
password:
```plaintext 
123456
```
grant_type password

credenciais da aplicação:
username:
```plaintext 
myclientid
```
password:
```plaintext 
myclientsecret
```
