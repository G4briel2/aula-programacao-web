# HTML, CSS e JavaScript

O desenvolvimento web é baseado em três tecnologias principais:

- **HTML** → estrutura da página  
- **CSS** → aparência/estilo  
- **JavaScript** → comportamento/interatividade  

---

# HTML (HyperText Markup Language)

O HTML é responsável por definir a **estrutura do conteúdo** da página.

Exemplo:

```html
<h1>Título</h1>
<p>Parágrafo</p>
```

Ele utiliza **tags** para organizar os elementos, como:
- `<h1>` a `<h6>` → títulos  
- `<p>` → parágrafos  
- `<img>` → imagens  
- `<a>` → links  

---

# CSS (Cascading Style Sheets)

O CSS é usado para definir o **visual da página**.

Permite alterar:
- Cores  
- Fontes  
- Espaçamentos  
- Layout  

Exemplo:

```css
h1 {
  color: blue;
  text-align: center;
}
```

---

# JavaScript (Vanilla JS)

### O que é JavaScript?

JavaScript é uma linguagem de programação utilizada para adicionar **interatividade** às páginas web.

Permite:
- Manipular elementos da página
- Responder a ações do usuário
- Atualizar conteúdo dinamicamente

---

# Como usar JavaScript

Pode ser utilizado de três formas:

### Inline
Dentro da própria tag HTML:
```html
<button onclick="alert('Olá')">Clique</button>
```

### Interno
Dentro da tag `<script>` no HTML:
```html
<script>
  alert("Olá");
</script>
```

### Externo (recomendado)
Arquivo separado:
```html
<script src="script.js"></script>
```

---

# Variáveis

Usadas para armazenar valores.

```js
let nome = "João";
const idade = 20;
```

- `let` → valor pode mudar  
- `const` → valor fixo  

---

# Tipos de Dados

Principais tipos:

- String → `"texto"`
- Number → `10`, `3.14`
- Boolean → `true` / `false`
- Null → ausência de valor
- Undefined → não definido

---

# Operadores

### Aritméticos
`+`, `-`, `*`, `/`

### Comparação
`==`, `===`, `!=`, `>`, `<`

### Lógicos
`&&` (E), `||` (OU), `!` (NÃO)

---

# Estruturas Condicionais

Permitem tomar decisões:

```js
if (idade >= 1{
  console.log("Maior de idade");
} else {
  console.log("Menor de idade");
}
```

---

# Funções

Blocos de código reutilizáveis:

```js
function saudacao(nome) {
  return "Olá " + nome;
}
```

---

# Eventos

Eventos são ações do usuário, como:

- Clique
- Digitação
- Movimento do mouse

Exemplo:

```js
button.addEventListener("click", function() {
  alert("Clicou!");
});
```

---

# Manipulação do DOM

O DOM representa a estrutura do HTML.

Permite alterar elementos da página:

```js
document.getElementById("titulo").innerText = "Novo texto";
```

---

## Integração entre HTML, CSS e JS

- HTML cria a estrutura  
- CSS estiliza  
- JavaScript adiciona comportamento 
