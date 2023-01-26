# api gateway micro servicos

- [ ] deve conter cadastros de clientes para cada micro servico
- [ ] deve conter os cadastros dos micro servicos
    - rotas
    - credenciais 
        - credenciais de cada micro servico ex JSON contendo endereco do BD e credenciais, de acordo com cada cliente
        - ```json 
            {
                cliente : {
                    cnpj : 111.1111.111/000-1,
                    acessos: [
                        {
                            servico: {
                                nome: servico,
                                enderecoAPI: url,
                                apiToken: ""
                            },
                            banco: "",
                            bancoToken: ""
                            
                        }
                    ],
                },

            }
            ```
- [ ] deve consumir api de OAuth mas prioridade é gateway.
- [ ] para uso da api gateway deve enviar payload com login e senha, (cpf ou cnpj do cliente)
- [ ] para rapidez do servico deve usar um dump ou um banco de dados em cache tipo redis por enquando um arquivo local
