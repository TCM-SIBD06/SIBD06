# C3 : SQL

## DDL

CREATE DATABASE IF NOT EXISTS `MarleyLizardo Yanick Cruz`;
USE `MarleyLizardo Yanick Cruz`;


DROP TABLE IF EXISTS Cliente;
DROP TABLE IF EXISTS Funcionario;
DROP TABLE IF EXISTS Area;
DROP TABLE IF EXISTS Encomenda;
DROP TABLE IF EXISTS Fornecedor;
DROP TABLE IF EXISTS Produto;
DROP TABLE IF EXISTS Equipamento;
DROP TABLE IF EXISTS Pagamento;
DROP TABLE IF EXISTS Assinatura;


CREATE TABLE IF NOT EXISTS Cliente 
( NumCliente int(11) unsigned NOT NULL, Nome varchar(50) NOT NULL, Idade int(3) unsigned NOT NULL, morada varchar(100) NOT NULL, telefone varchar(20) NOT NULL,PRIMARY KEY (NumCliente) )
ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS Funcionario 
( NumFuncionario int(11) unsigned NOT NULL, Nome varchar(50) NOT NULL, telefone int(11) unsigned NOT NULL, morada varchar(100) NOT NULL,PRIMARY KEY (NumFuncionario) )
ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS Area
(NumArea int(11) unsigned not null Auto_increment, nome varchar(50) NOT NULL, PRIMARY KEY (NumArea) ) 
ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS Fornecedor 
(NumFornecedor int(11) unsigned not null Auto_increment, nome varchar(50) COLLATE latin1_bin NOT NULL, morada varchar(50)  NOT NULL, Telefone varchar(20) NOT NULL, email varchar(50)  NOT null, PRIMARY KEY (NumFornecedor))
ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;


CREATE TABLE IF NOT EXISTS Produto
(NumProduto int(11) unsigned not null auto_increment, nome varchar(50) NOT NULL, PRIMARY KEY (NumProduto))
ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS Encomenda
( NumEncomenda int(11) unsigned NOT NULL, DataEntrega date NOT NULL, Quantidade int(4) COLLATE latin1_bin NOT null, NumFornecedor int(11) default null, PRIMARY KEY (NumEncomenda), KEY NumFornecedor (NumFornecedor) )
ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;



CREATE TABLE IF NOT EXISTS Equipamento
(NumEquipamento int(11) unsigned not null auto_increment,nome varchar(100) NOT NULL, preco int(11) unsigned NOT NULL, funcao varchar(10) NOT NULL, PRIMARY KEY (NumEquipamento) )
ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS Pagamento 
(NumPagamento int(11) unsigned not null auto_increment, DataPagamento date NOT NULL, TipoPagamento ENUM('MBway','Multibanco','Dinheiro'), valor int(10) unsigned NOT NULL, PRIMARY KEY (NumPagamento) ) 
ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS Assinatura 
(NumAssinatura int(11) unsigned not null auto_increment ,DataInicio date NOT NULL, DataFinal date NOT null, NumCliente int(11) default null, PRIMARY KEY (NumAssinatura), KEY NumCliente (NumCliente) )
ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;


CREATE OR REPLACE VIEW encomenda_view AS
SELECT e.NumEncomenda , e.DataEntrega , e.Quantidade, f.nome , f.morada , f.Telefone , f.email , f.NumFornecedor 
FROM encomenda e 
left join fornecedor f on f.NumFornecedor = e.NumFornecedor ; 

## DML

USE `MarleyLizardo Yanick Cruz`;

INSERT INTO Cliente (Numcliente, Nome , Idade, morada, telefone) VALUES (1,'João Rosário',24,'Alto de Pêga','914261225'), (2,'Maria Sousa',20,'Araújo','981595924') ,(3,'Carlos Andrade',30,'Árvore','958624759'),
(4,'Leonor Vicente',18,'Baguim','963568987' ), (5,'Marley Cardoso',25,'Bolhão','968475123'), (6,'Paula Maia', 17,'Botica','987654213' ), (7,'Lucas Basto',26,'Brito Capelo','974854623' ),
(8, 'Alice Silva',17,'Aliados','926253653'),(9,'Ana Santos',23,'Campainha','934425252'), (10,'Bárbara Ferreira',40,'Campanhã','952225445') ,(11,'Beatriz Pereira',45,'Campo 24 Agosto','954244545'),
(12,'Benedita Oliveira',42,'Cândido dos Reis','924524554'), (13,'Cármen Costa',31,'Carreira','945252544') ,(14,'Carolina Rodrigues',60,'Casa da Música','952524545'), (15,'Graça Martins',30,'Carolina Michaelis','925252555'),
(16,'Francisco Jesus',22,'Castelo da Maia','925244542'),(17,'Francisco Sousa',15,'Combatentes','952542445'), (18,'Gonçalo Fernandes',18,'Fânzeres','935245454'),(19,'Júlio Gonçalves',19,'Faria Guimarães','923642735'),
(20,'Manuel Gomes',26,'Fonte do Cuco','924254545'),(21,'Olívia Lopes',29,'Heroísmo','946436364'), (22,'Patrícia Marques',34,'João de Deus','934634646'), (23,'Rita Alves',41,'Mandim','946436344'),
(24,'Rosa Almeida',28,'Marquês','935643646'),(25,'Sílvia Ribeiro',64,'Matosinhos Sul','943634634'),(26,'Afonso Pinto',56,'Nau Vitória','943634637') ,(27,'António Carvalho',61,'Mandim','936434664'),
(28,'Benjamin Teixeira',52,'Trofa','934643464'), (29,'Miguel Moreira',55,'Fórum Maia','946446346'), (30,'Martim Correia',34,'Heroísmo','934646436');


INSERT INTO Funcionario (NumFuncionario, nome, telefone, morada) VALUES (2452,'Rui Barreira','962314785','Fórum Maia'), (2189,'Ruben Monteiro','951478236','Castelo da maia'), (1289,'Mariana Carvalho','963214587','Porto' ),
(5689,'Mariana Costa','932145786','Maia'), (3568,'Renata Barbosa','914568876','Porto' ), (1864,'António Monteiro','965484732','Maia');


INSERT INTO Area (nome) VALUES ('Personal Treiner'), ('Nutricionista'), ('Empregada'), ('Rececionista');


INSERT INTO Fornecedor (nome , morada, telefone,email) VALUES ('Fitness', 'Espinho', '965847121', 'Fitness@gmail.com'), ('Pingo Doce', 'Castelo da Maia', '808204545', 'cliente@pingodoce.pt'),
('Zumub', 'Lisboa', '707019426', 'info@zumub.pt');


INSERT INTO Encomenda (NumEncomenda , DataEntrega, Quantidade, NumFornecedor) VALUES (76800,'2022-08-10',2,1), (15322,'2023-09-04',1,1), (35225,'2022-06-08',1,2), (35235,'2022-07-01',3,3), (52553,'2022-07-04',4,1), (24542,'2022-10-09',6,2),
(42335,'2022-11-20',5,3);



INSERT INTO Produto (nome) VALUES ('Whey Protein'), ('Creatina'), ('Agua'), ('Barra de Proteína');


INSERT INTO Equipamento (nome , preco, funcao) VALUES ('FORCE USA MONSTER ULTIMATE LEG PRESS HACK SQUAT COMB', 2295,'Perna'), ('Banco de Musculação OUTSUNNY A91-031', 155, 'Peito'),
('Life Fitness Platinum Discover SE3HD Passadeira- Black Onyx', 12700 ,'cardio');


INSERT INTO Pagamento (DataPagamento , TipoPagamento, valor) VALUES ('2022-05-03', 'Multibanco', 10), ('2022-05-07', 'MBway' , 10), ('2022-05-09', 'Dinheiro', 10), ('2022-05-10', 'Multibanco', 10),
('2022-05-10', 'Dinheiro', 10), ('2022-05-02', 'MBway' , 10), ('2022-05-03', 'Dinheiro', 10), ('2021-05-03', 'Multibanco', 10), ('2021-05-08', 'MBway', 10), ('2021-04-03', 'Dinheiro', 10),
('2021-09-28', 'Multibanco', 10), ('2021-09-10', 'MBway', 10), ('2021-09-09', 'Multibanco', 10), ('2021-08-03', 'Dinheiro', 10), ('2021-12-03', 'MBway', 10), ('2021-01-10', 'Multibanco', 10),
('2021-03-03', 'Multibanco', 10), ('2022-05-31', 'Dinheiro', 10) ,('2022-03-03', 'MBway', 10), ('2022-04-22', 'Multibanco', 10), ('2022-09-03', 'Dinheiro', 10), ('2021-05-03', 'Dinheiro', 10),
('2022-05-07', 'Multibanco', 10), ('2021-09-09', 'Dinheiro', 10), ('2021-01-10', 'Dinheiro', 10), ('2021-09-08', 'MBway', 10), ('2022-05-10', 'MBway', 10), ('2022-05-01', 'Dinheiro', 10),
('2022-02-02','Dinheiro', 10), ('2022-03-11', 'Multibanco', 10), ('2022-05-03', 'Multibanco', 10);



INSERT INTO Assinatura (DataInicio , DataFinal) VALUES ('2022-05-03', '2023-05-03'), ('2022-05-07','2023-05-07'), ('2022-05-09','2023-05-09'), ('2022-05-10', '2023-05-10'), ('2022-05-10', '2023-05-10'),
('2022-05-02', '2023-05-02'), ('2022-05-03', '2023-05-03'), ('2021-05-03', '2022-05-03'), ('2021-05-08', '2022-05-08'), ('2021-04-03', '2021-04-05'), ('2021-09-28', '2022-09-28'), ('2021-09-10', '2022-09-10'),
('2021-09-09', '2022-09-09'), ('2021-08-03', '2022-08-03'), ('2021-12-03', '2022-12-03'), ('2021-01-10', '2022-01-10'), ('2021-03-03', '2022-03-03'), ('2022-05-31', '2023-05-31'), ('2023-03-03', '2023-03-03'),
('2022-04-22', '2023-04-22'), ('2022-09-03', '2023-09-03'), ('2021-05-03', '2022-05-03'), ('2022-05-07', '2023-05-07'), ('2021-09-09', '2022-01-10'), ('2021-01-10', '2023-01-10'), ('2021-09-28', '2023-09-28'),
('2022-05-10', '2023-05-10'), ('2022-05-01', '2023-05-01'), ('2022-02-02', '2023-02-02'), ('2022-03-11', '2023-03-11');



[< Previous](rebd04.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | Next >
:--- | :---: | ---: 
