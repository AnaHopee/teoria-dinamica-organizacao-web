# Atividade 2: Analisando a Validação de Formulários com JavaScript

## O que é Validação de Formulários

A validação de formulários é o processo de verificar se os dados inseridos em um formulário estão corretos e completos antes do envio. Com JavaScript, essa validação pode ser feita no lado do cliente, evitando requisições desnecessárias ao servidor e melhorando a experiência do usuário.

## Como JavaScript Captura e Valida os Dados

Usamos JavaScript para acessar os campos e seus valores:

```javascript
function validarFormulario() {
    let nome = document.getElementById("nome").value;
    if (nome === "") {
        alert("O campo nome é obrigatório.");
        return false;
    }
    return true;
}
````
*Expressões regulares (regex) são padrões utilizados para identificar sequências de caracteres. Elas são muito úteis para validar formatos específicos, como e-mails, números de telefone, etc.*

Exemplo: Validação de E-mail

````javascript
function validarEmail(email) {
    const regex = /^[a-zA-Z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$/;
    return regex.test(email);
}
`````

EXEMPLO COMPLETO DE VALIDAÇÃO:

````javascript

<form onsubmit="return validarFormulario()">
  <input type="text" id="email" placeholder="Digite seu e-mail">
  <button type="submit">Enviar</button>
</form>

<script>
function validarFormulario() {
    let email = document.getElementById("email").value;
    const regex = /^[a-zA-Z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$/;
    if (!regex.test(email)) {
        alert("E-mail inválido.");
        return false;
    }
    return true;
}
</script>
````

FONTES: 

https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Forms/Form_validation

https://www.w3schools.com/js/js_validation.asp

https://regex101.com/
