# C3 : Normalização

## Relações
Função_exercida (Funcionários→#_NºFuncionario_→ Area, _nome_) N/1

Regista (Encomendas→#_NºEncomenda_→Funcionários, _NºFuncionario, telefone, morada) 1/N

Esta_Incerida (Produtos→#_Nome_→ Encomendas, _, Data entrega, Quantidade) M/N

Enviado_Pelo (Encomendas→#_Nº_Encomenda_→Fornecedores, _nome_, morada, telefone, email) N/1

Forne-se (Fornecedores→#_nome_→ Produtos, _nome_)1/N

Forne-se (Fornecedores→#_nome → Equipamentos, _nome_, preço, função) 1/N

Concretrizado (Assinatura→#_data início_ → Pagamento, _data_, valor, tipo pagamento) 1/1

Executado (Assinatura→#_data início_ → Cliente, _ _ morada, nome, idade, telefone) N/M

## Normalização do Esquema Relacional
_(Apresentar o estudo da normalização das relações obtidas na secção anterior. Desnormalizar se necessário.)_

---
[< Previous](rebd02.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | [Next >](rebd04.md)
:--- | :---: | ---: 
