# C3 : Normalização

## Normalização do Esquema Relacional
Dependências Funcionais

1- Tabela Clientes:

(DF1) NºCliente→ nome

(DF2) NºCliente→ idade, morada, telefone

2- Tabela Funcionários:

(DF1) NºFuncionário→ nome

(DF2) NºFuncionário→ telefone, morada

(DF3) NºFuncionário, #areaNome→ nome, telefone, morada

(DF4) #areaNome→ nome, telefone, morada

3- Tabela Encomendas:

(DF1) NºEncomenda→ Data entrega

(DF2) NºEncomenda→ Quantidade

(DF3) NºEncomenda, #NºFuncionario→ Data entrega, Quantidade

4- Tabela Fornecedores:

(DF1) nome→ morada

(DF2) nome→ telefone, email

5- Tabela Equipamentos:

(DF1) nome→ preço

(DF2) nome→ função

(DF3) nome, #fornecedorNome→ preço, função

Normalização

Tabela Clientes:

1- NF

Clientes (NºClientes, nome, idade, morada, telefone

Chaves Candidatas: (NºClientes, nome) (NºClientes, idade, morada, telefone)

2- NF

Clientes (#NºClientes→idade, morada, telefone)

Chaves Candidatas: (NºClientes)

3- NF

(Sem alterações)

4- NF

(Sem alterações)

Tabela Funcionários:

1- NF

Funcionário (NºFuncionario, nome, telefone, morada)

Chaves Candidatas: (NºFuncionario, nome) (NºFuncionario, telefone, morada)

2- NF

Funcionário (#NºFuncionario→ telefone, morada)

Chave Candidatas:(NºFuncionario)

3- NF

Funcionário (#areaNome→nome, telefone, morada)

Chaves Candidatas (areaNome)

4- NF

Funcionário (#areaNome→ nome)

Chaves Candidatas (areaNome)

Tabela Encomendas:

1- NF

Encomendas (NºEncomenda, data entrega, quantidade)

Chaves Candidatas (NºEncomenda, data entrega) (NºEncomenda, quantidade)

2- NF

Encomendas (#NºEncomenda→ quantidade)

Chaves Candidatas (NºEncomenda)

3- NF

Encomendas (#NºFuncionario→data entrega, quantidade)

Chaves Candidatas (NºFuncionario)

4- NF

Encomendas (#NºFuncionario→quantidade)

Chaves Candidatas (NºFuncionario)

Tabela Fornecedor:

1- NF

Fornecedor (nome, morada, telefone, email)

Chaves Candidatas (nome, morada) (nome, telefone, email)

2- NF

Fornecedor (nome→ telefone, email)

Chaves Candidatas (nome)

3- NF

(Sem alterações)

4- NF

(Sem alterações)

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
