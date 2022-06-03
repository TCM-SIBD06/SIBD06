# C3 : Esquema conceptual

## Modelo E/A
![image](https://user-images.githubusercontent.com/96313629/171878733-9bfe0b2b-61c9-42d3-9525-12cca1f1ee75.png)

## Descrição
Entidades:

Client

Fornecedor

Funcionarios

Encomenda

Subscscrição                          

Pagamento 

Equipamentos

Produto

Atributo :

Cliente (nºCliente; morada ; nome ; idade; telefone) 

Funcionario (nªFuncionario; nome; telefone; morada; email)

Encomenda (nªEncomenda; data_ entrega; quantidade)

Produtos (nome)

Forncedor (nome; morada; telefone; email )

Equipamento (nom ; preço; função)

Area(nome)

Associações:

Função_Exercida (Funcionario;Area) N/1

Regista (Encomenda ; Funcionario)1/N

Esta_Incerida (Produtos; Encomenda) M/N

Enviado_Pelo (Encomenda; Fornecedor) N/M

Forne-se ( Forncedor; Produtos)N/M

Forne-se (Forncedor; Equipamentos) 1/N

Concretrizado (Subscrição ; Pagamento) 1/1

Executado (Subscrição ; Cliente) N/M





