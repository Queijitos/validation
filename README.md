

# Olá, eu sou a José Walter De Oliveira Junior! 👋
IIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIII
# Readme Sobre Email e CPF em JavaScript

Esses dois projetos de site são 1; sobre Como mandar um email ou ate mesmo salvar o email no site ou no sistema do PC, agora o projeto 2; seria o projeto de CPF onde você pode identificar se o CPF e real ou ele e falso.

---
# Projeto de Email   
O projeto do Email tem o Objetivo de conseguir ser um primerio passp para o PHP guardando informações no site, e fazendo o site avisar se o email esta errado ou Correto.
## Funcionalidades

- Descobrir se o Email esta correto ou Não
- salvar o email 
- Facil Funcionalidade 

## Exemplos do Codigo

[Documentação](cap1.png)
## Uso/Exemplos JS

```javascript
function ChecarEmail() {
    if (document.forms[0].email.value == "" ||
        document.forms[0].email.value.indexOf("@") == -1 ||
        document.forms[0].email.value.indexOf(".") == -1) {
        alert("Por favor informe um email valido");
        return false
    }else{
        alert("Email informado com sucesso!")
    }
}
```
# Projeto de CPF
O proejeto do CPF, teve a **funcionalidade** de apredizagem de como dar mais passos para o futuro do JavaScript e logo depois para o PHP, conseguindo provar se esta certo e errado.
## Funcionalidades

- Validar se o CPF e verdadeiro ou Falso
- salvar o CPF
- Facil Funcionalidade 

[Documentação](https://link-da-documentação)

## Uso/Exemplos JS

```javascript
// VALIDAÇÃO DE CPF

//adiciona um escutador
// -------------------------------------------------------------------------------------------------------------------
document.getElementById("cpfForm").addEventListener("submit", function (event) {
  event.preventDefault();

  const cpf = document.getElementById("cpf").value;
  const msg = document.getElementById("message");
  if(validateCPF(cpf)) {
    msg.textContent = 'O CPF é Valido';
    msg.style.color = 'green';
  }else {
    msg.textContent = 'O CPF e invalido';
    msg.style.color = 'red';
  }
});
// função de calculo de validação do CPF
// ----------------------------------------------------------------------------------------------------------
function validateCPF(cpf){
   cpf = cpf.replace(/[^\d]+/g, ''); //remove caracteres não numérico
 
// verificar se o valor contem 11 digitos e se todos os dígitos ão iguais
// --------------------------------------------------------------------------------------------------------
    if(cpf.length !== 11 || /^(\d)\1{10}$/.test(cpf)){
        return false;
    }
 let soma = 0;
 let resto;
 // --------------------------------------------------------------------------------------------------------
//  validação do primeiro digito verificador
for(let i = 1; i < 9; i++){
  soma += parseInt(cpf.substring(i-1, i)) * (11 - i)
}
resto (soma * 10 ) % 11;
  if((resto === 10) || (resto === 11)){
    resto = 0
  }
  if(resto !== parseInt(cpf.substring(9,10))){
 return false;
  }
 soma = 0;
 
 //validar 11 digito de CPF - 2°Digito verificador
 for( let i = 1; i <= 10; i++){
soma + parseInt( cpf.substring(i - 1, i))* (12 - i);
 }
 resto = (soma * 10) % 11;
 if((resto === 10) || (resto === 11)){
  resto = 0;
 }
 if(resto !== parseInt(cpf.substring(10,11))){
  return false;
 }
 return true;
}
```
# Ferramentas utilizadas
![CSS3](https://camo.githubusercontent.com/472c222e8f240a48ae51cd9b082a1b857be809dcd851a25150890c2da50c13a5/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f435353332d3135373242363f7374796c653d666f722d7468652d6261646765266c6f676f3d63737333266c6f676f436f6c6f723d7768697465)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)


