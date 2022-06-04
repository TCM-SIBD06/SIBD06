# C3 : Esquema conceptual

## Modelo E/A
![image](https://user-images.githubusercontent.com/96313629/171968346-a23bfd7d-07ed-4162-8788-8f9a616e3420.png)

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

## Regras de negócio adicionais (Restrições)
* Só é possivel ser feito as  assinaturas  dos clientes se isso for feito por um funcionario e esse funcionario tem que ser a reccecionita.
---
[< Previous](rebd01.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | [Next >](rebd03.md)
