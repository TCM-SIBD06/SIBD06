
# C4 : Esquema Relacional  <!-- omit in toc -->

# Clientes

## Descrição

Esta tabela irá guardar informações sobre os clientes.

## Colunas

| **Nome** | **Descrição** | **Domínio** | **por Omissão** | **Automático** | **Nulo** |
| --- | --- | --- | --- | --- | --- |
| **nCliente** | numero cliente | INT |  - | Sim |Não |
| **nome** | Nome do cliente. | VARCHAR(45) | - | Não | Não |
| **telemovel** | Telemóvel do cliente. | INT | - | Não | Não |
| **Idade** | idade  do  cliente.  | INT | -| Não | Não |

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| **Coluna(s)** |
| --------- |
| nºCliente



### Funcionarios 

#### DESCRIÇÃO <!-- omit in toc -->

Descrição dos funcinarios 

#### COLUNAS <!-- omit in toc -->

| **Nome**     | **Descrição**                 | **Domínio**     | **por Omissão** | **Automático** | **Nulo** |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| **NFuncionarios**  | numero de identidade dos funcinarios  | INT | Sim  | Não |
| **nome** | nome do funcionario | VARCHAR |  - | Não | Não |
|**morada** | morada do funcionario | VARCHAR (45) | - | Não | Não |
| **areaNome** | profissão dos funcionario | INT | - | Sim | Não |
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| **Coluna(s)** |
| --------- |
|NFuncionario |

- **Referêncial** (chaves estrangeiras)*:

| **Nome**  | **Coluna(s)** | **Tabela referênciada** | **Coluna(s) referênciada(s)** | **Indexar** |
| ----- | --------- | ------------------- | ------------------------- | ------- |
| FK\_Area\_ nome | nome profição | Area | nome |não |

### Area

#### DESCRIÇÃO <!-- omit in toc -->

Descrição das areas de profissão

#### COLUNAS <!-- omit in toc -->

| **Nome**     | **Descrição**                 | **Domínio**     | **por Omissão** | **Automático**| **Nulo** |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| nome | nome da area de  trabalho | INT| - | sim |Não |
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| **Coluna(s)** |
| --------- |
| Nome |

### Encomenda 

#### DESCRIÇÃO <!-- omit in toc -->

Descrição da tabela Encomenda 

#### COLUNAS <!-- omit in toc -->

| **Nome**     | **Descrição**                 | **Domínio**     | **por Omissão** | **Automático** | **Nulo** |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
|  **NEncomenda** | nome de encomenda | INT |  - | Não | Não |
| **Data_ Entrega** | data de entrega dos produtos | - | Sim | Não |
| **Quantidade** |  quantidade de  encomendas  | INT | - | sim | Não | 
|**NFuncionario** | Numero dos funcionario | INT  | - | Sim  | Não | 
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| **Coluna(s)** |
| --------- |
|NEncomenda |
- **Referêncial** (chaves estrangeiras)*:

| **Nome**  | **Coluna(s) | **Tabela referênciada** | **Coluna(s) referênciada(s)** | **Indexar** |
| ----- | --------- | ------------------- | ------------------------- | ------- |
| FK\_Funcionarios_ NFuncionarios | NFuncionarios | Funcionarios | NFuncionarios | Não  |

# ## Fornecedor 

## Descrição

Esta tabela irá guardar informações sobre os  Fornecedores.

## Colunas

| **Nome** | **Descrição** | **Domínio** | **por Omissão** | **Automático** | **Nulo** |
| --- | --- | --- | --- | --- | --- |
| **nome** | Nome do fornecedor | VARCHAR(200) | - | Sim | Não |
| **morada** | Morada do fornecedor | VArCHAR (200) | - | Não | Não |
| **telemovel** | Telemóvel do fornecedor | VARCHAR (45) | - | Não | Não |
| **Email** | Email do fornecedor | VARCHAR (45 ) | - | Não | Sim | 

## Restrições de Integridade


### Chave primária

| **Coluna(s)** |
| --- |
| Nome  |

### Produtos 

#### DESCRIÇÃO <!-- omit in toc -->

Descrição dos Produtos 

#### COLUNAS <!-- omit in toc -->

| **Nome**     | **Descrição**                 | **Domínio**     | **por Omissão** | **Automático**| **Nulo** |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| nome | nome dos produtos | INT | - | Sim | Não |
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| **Coluna(s)** |
| --------- |
| Nome |

### Equipamentos 

#### DESCRIÇÃO <!-- omit in toc -->

Descrição da tabela  Equipamentso 

#### COLUNAS <!-- omit in toc -->

| **Nome**     | **Descrição**                 | **Domínio**     | **por Omissão** | **Automático** | **Nulo** |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
|  **Nome | nome  dos equipamentos | VAUCHAR | - | Sim | Não | 
| **preço** | preço dos equipamentos | VAUCHAR | - | Não | Não | 
| **função** | função dos equipamento| VAUCHAR | - | Não | Sim | 
| **FornecedorNome** |nome dos fornecedores | INT | - | Sim | Não | 
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| **Coluna(s)** |
| --------- |
|nome |
- **Referêncial** (chaves estrangeiras)*:

| **Nome**  | **Coluna(s)** | **Tabela referênciada** | **Coluna(s) referênciada(s)** | **Indexar** |
| ----- | --------- | ------------------- | ------------------------- | ------- |
| FK\_Fornecedor_Nome  | Nome | Fornecedor | nome | não | 

### Pagamento

#### DESCRIÇÃO <!-- omit in toc -->

Descrição dos  Pagamentos 

#### COLUNAS <!-- omit in toc -->

| **Nome**     | **Descrição**                 | **Domínio**     | **por Omissão** | **Automático** | **Nulo** |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| data_ Pagamento | data dos pagamentos | INT | - | Sim | Não | 
| Tipo_ Pagamento |  tipo  de pagamento feito | VAUCHAR | - | Não | Não | 
| valor | valor  da Assinatura | VAUCHAR | - | Sim | Não | 
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| **Coluna(s)** |
| --------- |
| data Pagamento | 

### Subscrição  

#### DESCRIÇÃO <!-- omit in toc -->

Descrição das Subscrição 

#### COLUNAS <!-- omit in toc -->

| **Nome**     | **Descrição**                 | **Domínio**     | **por Omissão** | **Automático** | **Nulo** |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| data_ inicio | data que foi afetuado a assinatura |  INT | -  | Não | Não | 
| data_fim| data que a assinatura expira | INT | - | Sim | Não | 
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| **Coluna(s)** |
| --------- |
| data_ inicio | 

## Relações

### EstaIncerido 

#### DESCRIÇÃO <!-- omit in toc -->

Relação entre a  tabela Encomenda e  Produtos 

#### COLUNAS <!-- omit in toc -->

| **Nome**     | **Descrição**                 | **Domínio**     | **por Omissão** | **Automático** | **Nulo** |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
|NEncomenda | numero da encomenda | INT | - | Sim | Nao| 
| ProdutosNome | nome dos produtos | INT | - | Sim | Não |

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| **Coluna(s)** |
| --------- |
|NEncomenda | 
| Produtos Nome | 

- **Unicidade** (valores únicos)*:

| **Nome**        | **Coluna(s)** | **Indexar** |
| ----------- | --------- | ------- |
| Encomenda | NEconmenda | Não | 
| Produtos | Nome | Não | 

### Tem

#### DESCRIÇÃO <!-- omit in toc -->

Relação entre a  tabela Encomenda e Equipamentos . 

#### COLUNAS <!-- omit in toc -->

| **Nome**     | **Descrição**                 | **Domínio**     | **por Omissão** | **Automático** | **Nulo** |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
|NEncomenda | numero da encomenda | INT | - | Sim | No| 
| EquipamentoNome| nome do equipamento| INT | - | Sim | Não | 

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| Coluna(s) |
| --------- |
|NEncomenda | 
| EquipamentoNome| 

- **Unicidade** (valores únicos)*:

| **Nome**        | **Coluna(s)** | **Indexar** |
| ----------- | --------- | ------- |
| Encomenda | NEconmenda | Não | 
|  Equipamento | nome| Não |

### EnviadoPelo 

#### DESCRIÇÃO <!-- omit in toc -->

Relação entre a  tabela Encomenda e Fornecedor 

#### COLUNAS <!-- omit in toc -->

| **Nome**     | **Descrição**                | **Domínio**     | **por Omissão** | **Automático** | **Nulo** |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
|NEncomenda | numero da encomenda | INT | - | Sim | No| 
| FornecedorNome | nome do fornecedor | INT | - | Sim | Não | 

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| **Coluna(s)** |
| --------- |
|NEncomenda | 
| NomeFornecedor |

- **Unicidade** (valores únicos)*:

| **Nome**        | **Coluna(s)** | **Indexar** |
| ----------- | --------- | ------- |
| Encomenda | NEconmenda | Não | 
|  Fornecedor | Nome | Não | 

### Forne-se 

#### DESCRIÇÃO <!-- omit in toc -->

Relação entre a  tabela  produto  e fornecedor 

#### COLUNAS <!-- omit in toc -->

| **Nome**     | **Descrição**                 | **Domínio**     | **por Omissão** | **Automático** | **Nulo** |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
|ProdutoNome| nome do produto | INTER | - | Sim |  Não | 
| Fornecedor nome | nome do fornecedor | INTER | - | Não |  Não | 

#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| **Coluna(s)** |
| --------- |
|NomeProduto|
|NomeFornecedor |

- **Unicidade** (valores únicos)*:

| **Nome**        | **Coluna(s)** | **Indexar** |
| ----------- | --------- | ------- |
| Produto | Nome | Não | 
|  Fornecedor | Nome | Não | 

### RealizadoPor

#### DESCRIÇÃO <!-- omit in toc -->

Relação entre a  tabela  Subscrição e Pagamento

#### COLUNAS <!-- omit in toc -->

|  **Nome**     | **Descrição**                 | **Domínio**     | **por Omissão** | **Automático** | **Nulo** |
| :------- | :------------------------ | :---------- | :---------- | :--------- | :--- |
| **Data_Inicio** | data de inicio da assinatura | INT | - | Sim | Não | 
| **Data_ Pagamento** | data de  pagamento | INT | - | Sim | Não | 
| **idSubscrição** | identicação do pagamento | INT | - | Sim | Não | 
#### RESTRIÇÕES DE INTEGRIDADE <!-- omit in toc -->

- **Chave Primária**: 

| **Coluna(s**) |
| --------- |
|id|
| idSubscrição| 

- **Unicidade** (valores únicos)*:

| **Nome**        | **Coluna(s)** | **Indexar** |
| ----------- | --------- | ------- |
| Subscrição | idSubscrição| Não | 
| Pagamento |id | Não | 


---
| [< Previous](rebd03.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | [Next >](rebd05.md) |
| :---------------------- | :------------------------------------------------------: | ------------------: |



