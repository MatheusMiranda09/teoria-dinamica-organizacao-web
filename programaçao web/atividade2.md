A **validação de formulários no lado do cliente** usando **JavaScript** é uma prática comum no desenvolvimento web que tem como objetivo garantir que os dados inseridos pelo usuário estejam corretos **antes de serem enviados ao servidor**. Isso melhora a **experiência do usuário**, reduz a carga no servidor e previne o envio de dados inválidos.

---

### 🧩 Como funciona a validação com JavaScript

#### 1. **Captura dos dados do formulário**

JavaScript pode acessar os dados inseridos em um formulário HTML utilizando o DOM (Document Object Model). Por exemplo:

```html
<form id="meuFormulario">
  <input type="text" id="nome" name="nome">
  <input type="submit" value="Enviar">
</form>
```

```javascript
document.getElementById('meuFormulario').addEventListener('submit', function(event) {
  const nome = document.getElementById('nome').value;

  if (nome === '') {
    alert('O campo nome não pode estar vazio!');
    event.preventDefault(); // Impede o envio do formulário
  }
});
```

Neste exemplo:

* `addEventListener('submit', ...)` escuta o evento de envio do formulário.
* `.value` é usado para obter o valor digitado no campo.
* `event.preventDefault()` cancela o envio caso a validação falhe.

---

### ✅ Verificação de critérios específicos

Além de verificar se um campo está vazio, JavaScript pode validar:

* Comprimento mínimo/máximo de texto
* Números dentro de um intervalo
* Formatos específicos (ex: CPF, telefone, e-mail)
* Combinações de campos (ex: senha e confirmação de senha)

---

### ✳️ Expressões regulares (RegEx)

As **expressões regulares** são padrões utilizados para verificar se um texto corresponde a um determinado formato. Elas são muito úteis para validações mais complexas e precisas, como e-mails, números de telefone, CEPs, etc.

#### Exemplo: Validação de e-mail

```javascript
const email = document.getElementById('email').value;
const regexEmail = /^[a-zA-Z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$/i;

if (!regexEmail.test(email)) {
  alert('E-mail inválido!');
}
```

#### Explicação do padrão:

| Padrão              | Significado                                                           |
| ------------------- | --------------------------------------------------------------------- |
| `^`                 | Início da string                                                      |
| `[a-zA-Z0-9._%+-]+` | Parte local (antes do `@`) com letras, números, e símbolos permitidos |
| `@`                 | Caractere obrigatoriamente presente                                   |
| `[a-z0-9.-]+`       | Domínio (ex: gmail, uol, etc.)                                        |
| `\.`                | Ponto antes da TLD (ex: .com, .br)                                    |
| `[a-z]{2,}`         | TLD com no mínimo 2 letras (ex: com, br)                              |
| `$`                 | Fim da string                                                         |
| `/i`                | Ignora diferença entre maiúsculas e minúsculas                        |

---

### 💡 Conclusão

Validações com JavaScript no lado do cliente:

* Melhoram a usabilidade.
* Evitam requisições desnecessárias ao servidor.
* Podem usar expressões regulares para validações robustas.

Porém, **não substituem** a validação no servidor — que continua sendo essencial por questões de **segurança**.

---

### 📚 Fontes recomendadas:

* [MDN Web Docs – Client-side form validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation)
* [W3Schools – JavaScript Form Validation](https://www.w3schools.com/js/js_validation.asp)
* [Regex101 – ferramenta para testar expressões regulares](https://regex101.com/)
* [MDN Web Docs – Regular Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)

