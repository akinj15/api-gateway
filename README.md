# api AUTHORIZATION micro servicos

- [ ] deve conter cadastros de clientes para cada micro servico
- [ ] deve conter os cadastros dos micro servicos
    - rotas
        * GET /api/v1/credentials/:id
            ```javascript
                {
                    "user_id": "sha",
                    "authorization" : "token" // talvez necessario
                }
                // returns JSON 
                {
                    "cliente" : {
                        "user" : "cnpj || cpf || email",
                        "acessos": [
                            {
                                "servico": {
                                    "nome": "servico",
                                    "apiToken": "informed API TOKEN"
                                }
                            }
                        ]
                    }
                }
            ```
        * GET /api/v1/list-users
            ```javascript
                {
                    "user_id": "sha",
                    "authorization" : "token" // talvez necessario
                }
                // returns JSON 
                {
                    "cliente" : {
                        "user" : "cnpj || cpf || email",
                        "acessos": [
                            {
                                "servico": {
                                    "nome": "servico",
                                    "apiToken": "informed API TOKEN"
                                }
                            }
                        ]
                    }
                }
            ```            
        * POST /api/v1/create
            ```javascript
                {
                    "user": "cnpj || cpf || email",
                    "authorization" : "token", // talvez necessario
                    "acessos": ["api-1", "api-2", ...]
                }
                // returns JSON 
                {
                    "user_name": "cnpj || cpf || email",
                    "user_id": "sha",
                    "acessos": ["api-1", "api-2", ...] 
                }
            ```
        * PUT /api/v1/cliente/:id
            ```javascript
                {
                    "user_id": "sha",
                    "authorization" : "token", // talvez necessario
                    "acessos": ["api-1", "api-2", ...]
                }
                // returns JSON 
                {
                    "user_name": "cnpj || cpf || email",
                    "user_id": "sha",
                    "acessos": ["api-1", "api-2", ...] 
                }
            ```
        * DELETE /api/v1/cliente/:id
            ```javascript
                {
                    "user_id": "sha",
                    "authorization" : "token", // talvez necessario
                }
                // returns JSON 
                {
                    "user_name": "cnpj || cpf || email",
                    "user_id": "sha",
                }
            ```
    - credenciais 
        - JSON contendo credenciais e Servicos, de acordo com cada cliente

- [ ] deve consumir api de OAuth mas prioridade é API-AUTHORIZATION.
    * tempo de vida do token deve ser de 30 minutos.
- [ ] para uso da api gateway deve enviar payload com login e senha, (cpf ou cnpj do cliente)  
- [ ] para rapidez do servico deve usar um dump ou um banco de dados em cache tipo redis por enquando um arquivo local
