# Criando primeira fatura com a API

Agora vamos criar a sua primeira fatura via API, para que essa fatura seja criada com sucesso devemos  antes criar um token de acesso. Vamos agora montar um JSON que enviaremos no **BODY** da requisição

Para gerar esse token utilizarmos a rota **/v1/oauth/obtain_token**



```json
{
    "grantType": "clientCredentials",
    "clientId": "SEU Client ID",
    "clientSecret":"SEU CLIENT SECRET",
    "scopes": [
        "invoice",
    ]
}
```

### Resposta:


```json
{
    "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0eXBlIjoiY2xpZW50IiwiX293bmVySWQiOiI2MzZkM2RhNmY1MTVlMzAwMGExNWE4ZTEiLCJtZXRhZGF0YSI6eyJpcCI6IjEzMS4xNjEuOTIuMjEwIiwidXNlckFnZW50IjoiUG9zdG1hblJ1bnRpbWUvNy4zMC4wIiwiZ2VvbG9jYXRpb24iOnsiYWx0aXR1ZGUiOm51bGwsImxvbmdpdHVkZSI6bnVsbCwibGF0aXR1ZGUiOm51bGwsImFjY3VyYWN5IjpudWxsfX0sImlhdCI6MTY3MjY3MjcyNiwiZXhwIjoxNjcyNjczOTI2fQ.3Qvkgwmle2El3UD8Ml-kjDBH-pcvoYUx8yxufObXofA",
    "refreshToken": "QOUhVNvupIbGtxoq4aQQFt3K05a0wqIZ5hoWA0KweNirLYV7Afn8efnYK5l1K0o57qXMUpRLfGtF4bUZPX7YCLeLp619zGa7IrHyORBgW1u3kVNMa5eeCMB52fX58X3I",
    "expireAt": "2023-01-02T12:38:46.592-03:00",
    "refreshExpireAt": "2023-03-12T22:57:46.594-03:00"
}
```

