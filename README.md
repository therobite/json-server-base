
### Cadastro
<br/>
ENDPOINT   =>   /register ou /signup ou /users <br/>
<br/>

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários. exemplo de requisição:
    
            {
                "email":"teste@kenzie.com.br",
                "password":"12345678"
            }


Exemplo de retorno da API em caso de sucesso:

            {
                "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InRlc3RlQGtlbnppZS5jb20uYnIiLCJpYXQiOjE2NTY1Mjc3NjcsImV4cCI6MTY1NjUzMTM2Nywic3ViIjoiMiJ9.pmSMzoUC5Mv2s4OUz_t_gL5hsIJfd8xqpbCpzYpJ0ls",
                "user": {
                    "email": "teste@kenzie.com.br",
                    "id": 2
                }
            }

Exemplo PADRÃO de retorno da API em caso de erro:

            "Message error"



<hr/>


### Login
<br/>
ENDPOINT   =>   /login ou /signin <br/>
<br/>


Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"
<hr/>

### Configuração do PC 
<br/>
ENDPOINT   =>   /pcSpecs <br/>
<br/>

Endpoint para cadastrar e ver qual a configuração do PC do usuário
<br/>

Método GET:  *NÃO* é necessário estar logado
exemplo de retorno da API para método GET:

        [
            {
                "CPU": "i7-3770k",
                "motherboard": "z77x-d3h",
                "RAM": "8gb",
                "SSD": "240gb",
                "userId": 1,
                "id": 1
            }
        ]

Método POST:  *É* necessário estar logado e enviar o TOKEN na requisição, no body é OBRIGATÓRIO enviar o userId segue exemplo:

            {
                "CPU":"i7-3770k",
                "motherboard":"z77x-d3h",
                "RAM":"8gb",
                "SSD":"240gb",
                "userId": 1
            }

exemplo de retorno da API para método POST em caso de sucesso:


            {
                "CPU": "i7-3770k",
                "motherboard": "z77x-d3h",
                "RAM": "8gb",
                "SSD": "240gb",
                "userId": 1,
                "id": 1
            }

<hr/>

### Games Jogados

<br/>
ENDPOINT   =>   /pcSpecs <br/>
<br/>

Endpoint para cadastrar e ver qual os jogos jogados atualmente pelo usuário
<br/>

Método GET:  *É* necessário estar logado e enviar o TOKEN na requisição, exemplo de retorno da API em caso de sucesso:

        {
            "game": "Fortnite",
            "timePlayed": "13hrs",
            "plataform": "PC",
            "userId": 1,
            "id": 1
        }


Método POST: *É* necessário estar logado e enviar o TOKEN na requisição, no body é OBRIGATÓRIO enviar o userId:

            [
                {
                    "game": "Fortnite",
                    "timePlayed": "13hrs",
                    "plataform": "PC",
                    "userId": 1,
                    "id": 1
                }
            ]


<hr/>