# Criando a primeira faturas usando a API

Agora sim vamos criar a nossa fatura, vamos começar a montar o arquivo JSON, nele temos varias informações como dados do cliente dados do produto e endereço. Nesta demonstração usaremos somente os dados obrigatório para que a fatura seja criada, mas você pode consultar todos os outros parâmetros [aqui](/openapi/reference/operation/InvoicesController_createInvoice/)


Para gerar esse token utilizarmos a rota **/v1/invoices**

Nesta requisição vamos passar o parâmetro **Authorization** no header com o valor do token de acesso gerado [anteriormente](preparing-json-accessToken.md)


Usando o modo sandbox existes alguns usuário arios fictícios para ser usados, outros dados não será reconhecido pela API

## Dados usuários fictícios
<table>
    <tr>
        <td>Valerio de Aguiar Zorzato</td>
        <td>96050176876</td>
    </tr>
        <tr>
        <td>Joao da Costa Antunes	</td>
        <td>88398158808</td>
    </tr>
        <tr>
        <td>Valerio Alves Barros</td>
        <td>71943984190</td>
    </tr>
        <tr>
        <td>Joao da Costa Antunes</td>
        <td>97965940132</td>
    </tr>

</table>


Bearer

```json
{
    "client": {
        "treatmentPronoun": "you",
        "name": "Valerio de Aguiar Zorzato",
        "type": "pf",
        "cpfCnpj": "96050176876",
        "email": "valerio@gmail.com",
        "cellphone": "78798798798",
        "address": {

            "zip": "35170128",
            "city": "Coronel Fabriciano",
            "street": "Rua Doutor Moacir Byrro",
            "state": "MG",
            "zone": "Centro"
        }
    },
    "items": [
        {
            "name": "Notebook A315-58-573p I5 8gb 256gb Ssd 15,6",
            "quantity": 1,
            "value": 279900
        }

    ],
    "dueDate": "2023-12-30T23:59:59.999Z",
    "paymentMethods": {
        "pix": {
            "enable": true
        },
        "boleto": {
            "enable": true
        },
        "creditCard": {
            "enable": false
        }
    },
    "notifications":{
        "enable": false,
        "channels":{
            "sms":false,
            "email":true,
            "whatsApp":false
        },
        "types":{
            "daysBeforeExpiration3":true,
            "expirationDay":true,
            "invoiceCreate":true,
            "invoicePaid":true
        }
    },
    "cancelOverdue": false
}
```

<video width="100%" height="100%" loop controls>
  <source src="images/criar-fatura.mov" type="video/mp4">
</video>