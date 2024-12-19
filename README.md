##  API RESTful lançamentos bancários débito e crédito, Implementado com validação JWT. 

## ACESSO AO SWAGGER =>  http://localhost:8080/swagger-ui/index.html#/ 

## BANCO H2 ONLINE => http://localhost:8080/h2-console
- [X] username=sa 
- [X] password=sa
----------
### CADASTRO DE USUARIO VIA POSTMAN

- POST http://localhost:8080/usuarios 
#### BODY
- {
  -  "nome": "Usuario",
  -  "usuario": "usuario",
  -  "senha": "123",
  -  "roles": ["USERS","MANAGERS"]
-  }
----------
### PEGAR TOKEN VIA POSTMAN

- POST http://localhost:8080/login
#### BODY
- {
    -  "usuario": "usuario",
    -  "senha": "123",
-  }
----------
### REALIZAR LANCAMENTO DEBITO/CREDITO VIA POSTMAN
- POST http://localhost:8080/contas/lancamentos
#### BODY
- [
  - {
      -  "numeroConta": "12-123",
      -  "valor": 150.0,
      - "tipo": "CREDITO"
  -  },
  - {
      -  "numeroConta": "12-123",
      -  "valor":35.0,
      - "tipo": "DEBITO"
  -  }
- ]
----------
### OBTER SALDO DA CONTA VIA POSTMAN
- GET  http://localhost:8080/contas/12-123/saldo