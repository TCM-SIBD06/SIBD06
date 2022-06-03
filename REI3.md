# C3 : Esquema conceptual

## Modelo E/A
![MicrosoftTeams-image](https://user-images.githubusercontent.com/96313629/171834003-bb307d77-f478-47af-aa18-8a666a95a328.png)

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

Enviado_Pelo (Encomenda; Fornecedor) N/1

Forne-se ( Forncedor; Produtos)1/N

Forne-se (Forncedor; Equipamentos) 1/N

Concretrizado (Subscrição ; Pagamento) 1/1

Executado (Subscrição ; Cliente) N/M





