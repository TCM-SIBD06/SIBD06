# C3 : Esquema conceptual

## Modelo E/A
![Modelo EA](https://user-images.githubusercontent.com/96313629/167737625-0905ee0f-39cb-498d-a9d8-0d683953fc1f.png)

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



