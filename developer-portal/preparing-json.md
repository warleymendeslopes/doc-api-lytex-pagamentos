# Gerando o Token de acesso
:::attention
Para concluir este passo e nescessario que você tenha todos os documentos aprovados na plataforma 
:::

## Preparando o JSON

Usando a rota **/v1/oauth/obtain_token**, copie e altere o json abaixo com as informaçãoes de acordo com as credenciais informada no seu painel de configuraçao, se ainda nao configurou sua api [Clique aui para aprender como configurar](https://pay.lytex.com.br/auth/registration).

As posições do json a ser editadas são: 
- clientId </br>
Deve-se colocar o cliente ID 
- clientSecret </br>
Deve-se colocar o cliente ID 
- scopes </br>
Deve-se colocar as permissões que esse token precisa ter 



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


## Start the development environment

```bash
yarn start
```

This command will start a development server.
Most functionality exists in the development server except for search.
When the server is ready, the url will be published to the console.
It may default to http://localhost:3000.
Open that in a browser to see this developer portal load.

## Stop the development environment

Press control and c.

![control-c](ctrl-c.png)

## Clearing cache

:::warning
Troubleshooting? Try this out.
:::

A few changes (such as changing the key of a sidebar definition) require clearing cache to reflect in the local server.
We actively reduce these to make the best development environment experience possible.

1. Press control-c.
1. Run `yarn clean` in the command prompt to clear the cache.
1. Run `yarn start` again.


## Next steps

You are ready to train!

Go to the [training exercises list](index.md).


