
# C4 : Esquema Relacional  <!-- omit in toc -->

# Clientes

## Descrição

Esta tabela irá guardar informações sobre os clientes.

## Colunas

| **Nome** | **Descrição** | **Domínio** | **por Omissão** | **Automático** | **Nulo** |
| --- | --- | --- | --- | --- | --- |
| **nºCliente** | numero client | INT |  - | Sim |Não |
| **nome** | Nome do cliente. | VARCHAR(45) | - | Não | Não |
| **telemovel** | Telemóvel do cliente. | INT | - | Não | Não |
| **Idade** | idade  do  cliente.  | INT | -| Não | Não |

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| nºCliente



### Funcionarrios 

#### DESCRIÇÃO <!-- omit in toc -->

Descrição dos funcinario 

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| NºFuncionarios  | numero de identi dos funcinarios  | INT | Sim  | Não |
| nome | nome do funcionario | VARCHAR |  - | Não | Não |
|  morada | morada do funcionario | VARCHAR (45) | - | Não | Não |
| areaNome | profição dos funcionario | INT | - | Sim | Não |
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
|NºFuncionario |

- **Referêncial** (chaves estrangeiras)*:

| Nome  | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| ----- | --------- | ------------------- | ------------------------- | ------- |
| FK\_Area\_ nome | nome profição | Area | nome |não |

### Area

#### DESCRIÇÃO <!-- omit in toc -->

Descrição das areazs de profição 

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| nome | nomde da area de  trabalho | INT| - | sim |Não |
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| Nome |

### Encomenda 

#### DESCRIÇÃO <!-- omit in toc -->

Descrição da tabela Encomenda 

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
|  NªEncomenda | numde de encomenda | INT |  - | Não | Não |
| Dat _ Entrega | data de entrega dos produtos | - | Sim | Não |
| Quantidade |  quantidade de  encomendas  | INT | - | sim | Não | 
|NºFuncionario | Numero dos funcionario | INT  | - | Sim  | Não | 
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
|NºEncomenda |
- **Referêncial** (chaves estrangeiras)*:

| Nome  | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| ----- | --------- | ------------------- | ------------------------- | ------- |
| FK\_Funcionarios_ NºFuncionarios | Nº Funcionarios | Funcionarios | Nº Funcionarios | Não  |

# ## Fornecedor 

## Descrição

Esta tabela irá guardar informações sobre os  Fornecedores.

## Colunas

| **Nome** | **Descrição** | **Domínio** | **por Omissão** | **Automático** | **Nulo** |
| --- | --- | --- | --- | --- | --- |
| **nome** | Nome do fornecedor | VARCHAR(200) | - | Sim | Não |
| **morada** | Morada do fornecedor | VArCHAR (200) | - | Não | Não |
| **telemovel** | Telemóvel do fornecedor | VARCHAR (45) | - | Não | Não |
| **Email** | Email do f ornecedor | VARCHAR (45 ) | - | Não | Sim | 

## Restrições de Integridade


### Chave primária

| **Coluna(s)** |
| --- |
| Nome  |

### Produtos 

#### DESCRIÇÃO <!-- omit in toc -->

Descrição dos Produtos 

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| nome | nomde dos produtos | INT | - | Sim | Não |
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| Nome |

### Equipamentos 

#### DESCRIÇÃO <!-- omit in toc -->

Descrição da tabela  Equipamentso 

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
|  Nome | nome  dos equipamentos | VAUCHAR | - | Sim | Não | 
| preço | preço dos equipamentos | VAUCHAR | - | Não | Não | 
| função | função dos equipamento| VAUCHAR | - | Não | Sim | 
| FornecedorNome |nome dos fornecedors | INT | - | Sim | Não | 
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
|nome |
- **Referêncial** (chaves estrangeiras)*:

| Nome  | Coluna(s) | Tabela referênciada | Coluna(s) referênciada(s) | Indexar |
| ----- | --------- | ------------------- | ------------------------- | ------- |
| FK\_Fornecedor_Nome  | Nome | Fornecedor | nome | não | 

### Pagamento

#### DESCRIÇÃO <!-- omit in toc -->

Descrição dos  Pagamentso 

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| data_ Pagamento | data dos pagamentso | INT | - | Sim | Não | 
| Tipo_ Pagamento |  tipo  de pagamento feito | VAUCHAR | - | Não | Não | 
| valor | valo  da Assinatura | VAUCHAR | - | Sim | Não | 
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| data Pagamento | 

### Assinatura 

#### DESCRIÇÃO <!-- omit in toc -->

Descrição dos  Pagamentso 

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| data_ inicio | data que foi afetuado a assinatura |  INT | -  | Não | Não | 
| data_fim| data que a assinatura expira | INT | - | Sim | Não | 
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
| data_ inicio | 

## Relações

### EstaIncerido 

#### DESCRIÇÃO <!-- omit in toc -->

Relação entre a  tabela Encomenda e  Produtos 

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
|NºEncomenda | numero da encomenda | INT | - | Sim | No| 
| ProdutosNome | nome dos produtos | INT | - | Sim | Não

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
|Nº Encomenda | 
| Produtos Nome | 

- **Unicidade** (valores únicos)*:

| Nome        | Coluna(s) | Indexar |
| ----------- | --------- | ------- |
| Encomenda | Nº Econmenda | Não | 
| Produtos | Nome | Não | 

### EstaIncerido 

#### DESCRIÇÃO <!-- omit in toc -->

Relação entre a  tabela Encomenda e Equipamentos . 

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
|NºEncomenda | numero da encomenda | INT | - | Sim | No| 
| Equipamento Nome| nome do equipamento| INT | - | Sim | Não | 

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
|Nº Encomenda | 
| Equipamento Nome| 

- **Unicidade** (valores únicos)*:

| Nome        | Coluna(s) | Indexar |
| ----------- | --------- | ------- |
| Encomenda | Nº Econmenda | Não | 
|  Equipamento | nom| Não |

### Enviado Pelo 

#### DESCRIÇÃO <!-- omit in toc -->

Relação entre a  tabela Encomenda e Fornecedor 

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
|NºEncomenda | numero da encomenda | INT | - | Sim | No| 
| Fornecedor Nome | nom do fornecedor | INT | - | Sim | Não | 

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
|Nº Encomenda | 
| Nome Fornecedor |

- **Unicidade** (valores únicos)*:

| Nome        | Coluna(s) | Indexar |
| ----------- | --------- | ------- |
| Encomenda | Nº Econmenda | Não | 
|  Fornecedor | Nome | Não | 

### Forne-se 

#### DESCRIÇÃO <!-- omit in toc -->

Relação entre a  tabela  produto  e fornecedor 

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
|Produto Nome| nome do produto | INTER | - | Sim |  Não | 
| Fornecedor nome | nome do fornecedor | INTER | - | Não |  Não | 

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
|Nome Produto|
|Nome Fornecedor |

- **Unicidade** (valores únicos)*:

| Nome        | Coluna(s) | Indexar |
| ----------- | --------- | ------- |
| Produto | Nome | Não | 
|  Fornecedor | Nome | Não | 

### Executado 

#### DESCRIÇÃO <!-- omit in toc -->

Relação entre a  tabela  Assinatura e Pagamento

#### COLUNAS <!-- omit in toc -->

| Nome     | Descrição                 | Domínio     | por Omissão | Automático | Nulo |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| Data_Inicio | data de inicio da assinatura | INT | Sim | Não | 
| Data_ Pagamento | data de  pagamento | INT | Sim | Não | 

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
|data_Inicio |
|data_pagamento| 

- **Unicidade** (valores únicos)*:

| Nome        | Coluna(s) | Indexar |
| ----------- | --------- | ------- |
| Assinatura | data_Inicio| Não | 
| Pagamento | data_Pagamento | Não | 


---
| [< Previous](rebd03.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | [Next >](rebd05.md) |
| :---------------------- | :------------------------------------------------------: | ------------------: |



