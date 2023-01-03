# Criando token de acesso

Agora com a integração criada e configurada dentro do painel da lytex vamos utilizar o Postman para gerar o token de acesso e também a primeira fatura, primeiramente e necessário montar o arquivo JSON, como o arquivo abaixo você pode copiar e colar ele no seu Postman. Apos colocar seus dados da integração basta executar e recebera uma resposta de nossa API com um parâmetro chamado **accessToken**, e também receberemos como parâmetros algumas informações referente a esse token. Lembrando que esse token tem a durabilidade de 5min

Feito isso e ja tendo o **accessToken** salvo podemos passar para o [próximo passo](create-invoices.md) a geração de faturas


Para gerar esse token utilizarmos a rota **/v1/oauth/obtain_token**


```json
{
    "grantType": "clientCredentials",
    "clientId": "SEU Client ID",
    "clientSecret":"SEU CLIENT SECRET",
    "scopes": [
        "invoice"
    ]
}
```



<video width="100%" height="100%"  autoplay loop controls>
  <source src="images/criando-token-de-acesso.mov" type="video/mp4">
</video>







