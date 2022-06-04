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
Dependências Funcionais

Tabela Clientes:
(DF1) NºCliente→ nome

(DF2) NºCliente→ idade, morada, telefone



Tabela Funcionários:
(DF1) NºFuncionário→ nome

(DF2) NºFuncionário→ telefone, morada

(DF3) NºFuncionário, #areaNome→ nome, telefone, morada

(DF4) #areaNome→ nome, telefone, morada



Tabela Encomendas:
(DF1) NºEncomenda→ Data entrega

(DF2) NºEncomenda→ Quantidade

(DF3) NºEncomenda, #NºFuncionario→ Data entrega, Quantidade



Tabela Fornecedores:
(DF1) nome→ morada

(DF2) nome→ telefone, email



Tabela Equipamentos:
(DF1) nome→ preço

(DF2) nome→ função

(DF3) nome, #fornecedorNome→ preço, função



Normalização

Tabela Clientes:

NF
Clientes (NºClientes, nome, idade, morada, telefone

Chaves Candidatas: (NºClientes, nome) (NºClientes, idade, morada, telefone)





NF
Clientes (#NºClientes→idade, morada, telefone)

Chaves Candidatas: (NºClientes)

NF
(Sem alterações)

NF
(Sem alterações)



Tabela Funcionários:

NF
Funcionário (NºFuncionario, nome, telefone, morada)

Chaves Candidatas: (NºFuncionario, nome) (NºFuncionario, telefone, morada)

NF
Funcionário (#NºFuncionario→ telefone, morada)

Chave Candidatas:(NºFuncionario)

NF
Funcionário (#areaNome→nome, telefone, morada)

Chaves Candidatas (areaNome)

NF
Funcionário (#areaNome→ nome)

Chaves Candidatas (areaNome)



Tabela Encomendas:

NF
Encomendas (NºEncomenda, data entrega, quantidade)

Chaves Candidatas (NºEncomenda, data entrega) (NºEncomenda, quantidade)

NF
Encomendas (#NºEncomenda→ quantidade)

Chaves Candidatas (NºEncomenda)





NF
Encomendas (#NºFuncionario→data entrega, quantidade)

Chaves Candidatas (NºFuncionario)

NF
Encomendas (#NºFuncionario→quantidade)

Chaves Candidatas (NºFuncionario)



Tabela Fornecedor:

NF
Fornecedor (nome, morada, telefone, email)

Chaves Candidatas (nome, morada) (nome, telefone, email)

NF
Fornecedor (nome→ telefone, email)

Chaves Candidatas (nome)

NF
 (Sem alterações)

NF
(Sem alterações

Tabela  Equipamentos :

1-	NF 

Equipamento(Nome ; preço ; função)

Chave Candidata ( nome, preço) (nome, função )

2-	NF 

Equipamentos (# nome→  função )

Chave Candidata ( nome) 

3-	NF

Equipamentos (#FornecedorNome → preço , função)

Chave candidata (FornecedorNome  )

4-	NF

Equipamentos ( #FornecedorNome → função )

Chave candidata (FornecedorNome  )


---
[< Previous](rebd02.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | [Next >](rebd04.md)
:--- | :---: | ---: 
