# C3 : SQL

## DDL

USE `MarleyLizaerdo e Yanick da Cruz`;

DROP TABLE IF EXISTS `Clientes`;
DROP TABLE IF EXISTS `Funcionario`;
DROP TABLE IF EXISTS `Area`;
DROP TABLE IF EXISTS `Encomenda`;
DROP TABLE IF EXISTS `Fornecedores`;
DROP TABLE IF EXISTS `Produtos`;
DROP TABLE IF EXISTS `Equipamentos`;
DROP TABLE IF EXISTS `Pagamentos`;




CREATE TABLE IF NOT EXISTS `Clientes` (
  `NºCliente` int(4) unsigned NOT NULL,
  `Nome` int(4) unsigned NOT NULL,
  `Idade` int(3) unsigned NOT NULL,
  `morada` float unsigned NOT NULL,
  `telefone` float unsigned NOT NULL,
  
  PRIMARY KEY (`NºCliente`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS `Funcionário` (
  `NºFuncionario` int(4) unsigned NOT NULL,
  `Nome` int(4) unsigned NOT NULL,
  `telefone` int(3) unsigned NOT NULL,
  `morada` float unsigned NOT NULL,
  
  PRIMARY KEY (`NºFuncionario`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS `Area` (
  `nome` int(4) unsigned NOT NULL,
  PRIMARY KEY (`nome`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS `Encomenda` (
  `NºEncomenda` varchar(2) COLLATE latin1_bin NOT NULL,
  `Data Entrega` int(4) unsigned NOT NULL,
  `Quantidade` varchar(8) COLLATE latin1_bin NOT NULL,
  PRIMARY KEY (`NºEncomenda`),
  KEY `Fornecedores` (`nome`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS `Fornecedores` (
  `nome` varchar(2) COLLATE latin1_bin NOT NULL,
  `morada` int(4) unsigned NOT NULL,
  `Telefone` varchar(8) COLLATE latin1_bin NOT NULL,
   `email` int(4) unsigned NOT NULL,
)
 CREATE TABLE IF NOT EXISTS `Produtos` (
  `nome` int(4) unsigned NOT NULL,
  
  PRIMARY KEY (`nome`)

) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS `Equipamentos` (
  `nome` int(4) unsigned NOT NULL,
  `preço` int(4) unsigned NOT NULL,
  `função` int(3) unsigned NOT NULL,
 PRIMARY KEY (`nome`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS `Pagamento` (
  `data pagamento` int(4) unsigned NOT NULL,
  `tipo pagamento` int(4) unsigned NOT NULL,
  `valor` int(3) unsigned NOT NULL,
 PRIMARY KEY (`data pagamento`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;

CREATE TABLE IF NOT EXISTS `Assinatura` (
  `data inicio` int(4) unsigned NOT NULL,
  `data Final` int(4) unsigned NOT NULL,
  PRIMARY KEY (`data inicial`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_bin;


START TRANSACTION;

INSERT INTO `Clientes` (`Nºcliente`, `nome`, `idade`, `morada`, `telefone`) VALUES
(01,João Rosário,24,Alto de Pêga,914261225)
(02,Maria Sousa,20,Araújo,981595924 )
(03,Carlos Andrade,30,Árvore,958624759)
(04,Leonor Vicente,18,Baguim,963568987 )
(05,Marley Cardoso,25,Bolhão,968475123)
(06,Paula Maia, 17,Botica,987654213 )
(07,Lucas Basto,26,Brito Capelo,974854623 )
(08, Alice Silva,17,Aliados,926253653)
(09,Ana Santos,23,Campainha,934425252)
(10,Bárbara Ferreira,40,Campanhã,952225445)
(11,Beatriz Pereira,45,Campo 24 Agosto,954244545)
(12,Benedita Oliveira,42,Cândido dos Reis,924524554)
(13,Cármen Costa,31,Carreira,945252544)
(14,Carolina Rodrigues,60,Casa da Música,952524545)
(15,Graça Martins,30,Carolina Michaelis,925252555)
(16,Francisco Jesus,22,Castelo da Maia,925244542)
(17,Francisco Sousa,15,Combatentes,952542445)
(18,Gonçalo Fernandes,18,Fânzeres,935245454)
(19,Júlio Gonçalves,19,Faria Guimarães,923642735)
(20,Manuel Gomes,26,Fonte do Cuco,924254545)
(21,Olívia Lopes,29,Heroísmo,946436364)
(22,Patrícia Marques,34,João de Deus,934634646)
(23,Rita Alves,41,Mandim,946436344)
(24,Rosa Almeida,28,Marquês,935643646)
(25,Sílvia Ribeiro,64,Matosinhos Sul,943634634)
(26,Afonso Pinto,56,Nau Vitória,943634637)
(27,António Carvalho,61,Mandim,936434664)
(28,Benjamin Teixeira,52,Trofa,934643464)
(29,Miguel Moreira,55,Fórum Maia,946446346)
(30,Martim Correia,34,Heroísmo,934646436)


INSERT INTO `Funcionario` (`NºFuncionario`, `nome`, `telefone`, `morada`) VALUES
(2452,Rui Barreira,962314785,Fórum Maia)
(2189,Ruben Monteiro,951478236,Castelo da maia)
(1289,Mariana Carvalho,963214587,Porto )
(5689,Mariana Costa,932145786,Maia)
(3568,Renata Barbosa,914568876,Porto )
(1864,António Monteiro,965484732,Maia)

INSERT INTO `area` (`nome`) VALUES
(Personal Treiner)
(Nutricionista)
(Empregada)
(Rececionista)


INSERT INTO `Encomenda` (`NºEncomenda` , `Data Entrega`, `Quantidade`) VALUES
(76800,10/8/2022,2)
(15322,4/9/2023,1)
(35225,8/6/2022,1)
(35235,1/7/2022,3)
(52553,4/7/2022,4)
(24542,9/10/2022,6)
(42335,20/11/2022,5)

INSERT INTO `Fornecedores` (`nome` , `morada`, `telefone`,`email`) VALUES
(Fitness,	Espinho,	965847121,	Fitness@gmail.com)
(Pingo Doce,	Castelo da Maia,	808204545,	cliente@pingodoce.pt)
(Zumub,	Lisboa,	707019426,	info@zumub.pt)

INSERT INTO `Produtos` (`nome`) VALUES
(Whey Protein)
(Creatina)
(Agua)
(Barra de Proteína)

INSERT INTO `Equipamentos` (`nome` , `preço`, `função`) VALUES
(FORCE USA MONSTER ULTIMATE LEG PRESS HACK SQUAT COMB,	2295,	Perna)
(Banco de Musculação OUTSUNNY A91-031,	155,	Peito)
(Life Fitness Platinum Discover SE3HD Passadeira- Black Onyx,	12700	,cardeio)

INSERT INTO `Pagamentos` (`data pagamento` , `tipo pagamento`, `valor`) VALUES
(3/5/2022,	Multibanco,	10)
(7/5/2022,	MBway	, 10)
(9/5/2022,	Dinheiro, 10)
(10/5/2022,	Multibanco,	10)
(10/5/2022,	Dinheiro,	10)
(2/5/2022,	MBway ,	10)
(3/5/2022,	Dinheiro,	10)
(3/5/2021,	Multibanco,	10)
(8/5/2021,	MBway,	10)
(3/4/2021,	Dinheiro,	10)
(28/9/2021,	Multibanco,	10)
(10/9/2021,	MBway,	10)
(9/9/2021,	Multibanco,	10)
(3/8/2021,	Dinheiro,	10)
(3/12/2021,	MBway,	10)
(10/1/2021,	Multibanco,	10)
(3/3/2021,	Multibanco,	10)
(31/5/2022,	Dinheiro,	10)
(3/3/2022,	MBway,	10)
(22/4/2022,	Multibanco,	10)
(3/9/2022,	Dinheiro,	10)
(3/5/2021,	Dinheiro,	10)
(7/5/2022,	Multibanco,	10)
(9/9/2021,	Dinheiro,	10)
(10/1/2021,	Dinheiro,	10)
(8/9/2021,	MBway,	10)
(10/5/2022,	MBway,	10)
(1/5/2022,	Dinheiro,	10)
(2/2/2022,Dinheiro,	10)
(11/3/2022,	Multibanco,	10)
(3/5/2022,	Multibanco,	10)

NSERT INTO `Assinatura` (`data inicio` , `data final`) VALUES
(3/5/2022,	3/5/2023)
(7/5/2022,	7/5/2023)
(9/5/2022,	9/5/2023)
(10/5/2022,	10/5/2023)
(10/5/2022,	10/5/2023)
(2/5/2022,	2/5/2023)
(3/5/2022,	3/5/2023)
(3/5/2021,	3/5/2022)
(8/5/2021,	8/5/2022)
(3/4/2021,	3/4/2022)
(28/9/2021,	28/9/2022)
(10/9/2021,	10/9/2022)
(9/9/2021,	9/9/2022)
(3/8/2021,	3/8/2022)
(3/12/2021,	3/12/2022)
(10/1/2021,	10/1/2022)
(3/3/2021,	3/3/2022)
(31/5/2022,	31/5/2023)
(3/3/2022,	3/3/2023)
(22/4/2022,	22/4/2023)
(3/9/2022,	3/9/2023)
(3/5/2021,	3/5/2022)
(7/5/2022,	7/5/2023)
(9/9/2021,	10/1/2022)
(10/1/2021,	10/1/2023)
(28/9/2021,	28/9/2023)
(10/5/2022,	10/5/2023)
(1/5/2022,	1/5/2023)
(2/2/2022,	2/2/2023)
(11/3/2022,	11/3/2023)


[< Previous](rebd04.md) | [^ Main](https://github.com/exemploTrabalho/reportSIBD/) | Next >
:--- | :---: | ---: 
