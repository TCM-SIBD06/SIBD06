# C3 : Esquema conceptual

## Modelo E/A
![DiagramaFinal ](https://user-images.githubusercontent.com/96313629/174460991-bcaed8d5-dc4f-412f-89a4-358e01ea55e0.png)
## Descrição


### Atributos

Clientes (_ncliente_ , nome , morada , idade , telefone) 

Funcionarios (_nFuncionario_ , nome , telefone , morada , email)

Encomenda (_nEncomenda_ , data entrega , quantidade)

Produtos (_nome_)

Forncedor (_nome_ , morada , telefone , email)

Equipamento (_nome_ , preço , função)

Area (_nome_)

### Associações

Função_Exercida (Funcionarios;Area) N/1

Regista (Encomenda ; Funcionarios)1/N

Esta_Incerida (Produtos; Encomenda) M/N

Enviado_Pelo (Encomenda; Fornecedor) N/M

Forne-se ( Forncedor; Produtos)N/M

Tem (Forncedor; Equipamentos) 1/N

RealizadoPor (Subscrição ; Pagamento) 1/1

ExecutadoPelo (Subscrição ; Clientes) N/M

## Regras de negócio adicionais (Restrições)
* Só é possivel ser feito as  assinaturas  dos clientes se isso for feito por um funcionario e esse funcionario tem que ser a reccecionita.
---
[< Previous](rebd01.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | [Next >](rebd03.md)
