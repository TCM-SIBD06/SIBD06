# C3 : Esquema conceptual

## Modelo E/A
![DiagramaFinal ](https://user-images.githubusercontent.com/96313629/174461249-4fc7bddd-9b07-47f6-a1e6-8316ba2e7442.png)
## Descrição


### Atributos

Subscrição(_idSubscrição_ , data_inicio , data_final)

Clientes (_ncliente_ , nome , morada , idade , telefone) 

Funcionarios (_nFuncionario_ , nome , telefone , morada , email)

Encomenda (_nEncomenda_ , data entrega , quantidade)

Produtos (_nome_)

Fornecedor (_nome_ , morada , telefone , email)

Equipamento (_nome_ , preço , função)

Area (_nome_)

Pagamento (_id_, data , valor)

### Associações

Função_Exercida (Funcionarios;Area) N:1 Total/Total

Regista (Encomenda ; Funcionarios)1:N total/parcial

Esta_Incerida (Produtos; Encomenda) M:N parcial/Total

Enviado_Pelo (Encomenda; Fornecedor) N:M  parcial/parcial

Forne-se ( Forncedor; Produtos)N/M Total/parcial

Tem (Forncedor; Equipamentos) 1/N Total/parcial

RealizadoPor (Subscrição ; Pagamento) 1/1 Total/Total

ExecutadoPelo (Subscrição ; Clientes) N/M  Total/Total

## Regras de negócio adicionais (Restrições)
* Só é possivel ser feito as  assinaturas  dos clientes se isso for feito por um funcionario e esse funcionario tem que ser a reccecionita.
---
[< Previous](rebd01.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | [Next >](rebd03.md)
