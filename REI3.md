# C3 : Esquema conceptual

## Modelo E/A
![MicrosoftTeams-image](https://user-images.githubusercontent.com/96313629/171834003-bb307d77-f478-47af-aa18-8a666a95a328.png)

## Descrição
Entidades:

Ginásio 

Client

FornecedorDeEquipamento

FornecedorDeSuplemento

FornecedorDeAgua

PersonaTreinar 

Nutricionista 

Empregada

Rececionista

Atributo:

Ginásio ( nome ; localização; nºDeClientes ; empregados; nªTelefone)

Cliente (nºCliente; morada ; nªTelemovel)

FornecedorDeEquipamento( nome ; localização; nªTelemovel ; email ; limiteDeFornecimento )

FornecedorDeSuplemento ( nome; limiteDeFornecimento ; localização; nªTelemovel ; email )

FornecedorDeAgua ( nome; limiteDeFornecimento ; localização; nªTelemovel  ;email )

PersonalTreinar (nºDeFuncionario; nome; morada; nªTelemovel; email; areaEspecializada)

Nutricionista (nºDeFuncionario; nome; morada; nªTelemovel; email; areaEspecializada)

Empregada (nºDeFuncionario; nome; morada; nªTelemovel; email)

Rececionista (nºDeFuncionario; nome; morada; nªTelemovel; email)

Associações:

frequentaO (Cliente; Ginasio)

fornece (fornecedorDeEquipamento; Ginásio )

fornece (fornecedorDeSuplemento; Ginásio )

fornece (fornecedorDeAgua; Ginásio )

DaTreino ( PersonalTreinar ; Cliente )

AtendeOs (Rececionista; Cliente)

Consulta (Nutricionista ; Cliente)

trabalhaNo (Cliente ; Ginásio)

LimpaO (Empregada; Ginásio)



