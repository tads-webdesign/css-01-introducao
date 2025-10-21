# Introdução ao CSS: Seletores, Propriedades e Valores

## O que é CSS e como funciona

**CSS** (Cascading Style Sheets - Folhas de Estilo em Cascata) é uma linguagem de estilo utilizada para descrever a apresentação de documentos HTML. Enquanto o HTML define a estrutura e o conteúdo de uma página web, o CSS é responsável pela aparência visual: cores, fontes, espaçamentos, layouts e muito mais.

### Como o CSS funciona?

O CSS funciona aplicando regras de estilo aos elementos HTML. Cada regra CSS consiste em:

1. **Seletor**: Indica qual(is) elemento(s) HTML será(ão) estilizado(s)
2. **Propriedades**: Características visuais que queremos modificar
3. **Valores**: As configurações específicas para cada propriedade

**Estrutura básica de uma regra CSS:**

```css
seletor {
    propriedade: valor;
    outra-propriedade: outro-valor;
}
```

**Exemplo:**

```css
p {
    color: blue;
    font-size: 16px;
}
```

Neste exemplo:
- `p` é o **seletor** (seleciona todos os parágrafos)
- `color` e `font-size` são **propriedades**
- `blue` e `16px` são os **valores**

---

## Formas de Aplicar CSS

Existem três formas principais de aplicar CSS a um documento HTML:

### 1. CSS Inline (Embutido)

O CSS é aplicado diretamente no elemento HTML usando o atributo `style`.

**Exemplo:**

```html
<p style="color: red; font-size: 18px;">Este é um parágrafo vermelho.</p>
```

**Vantagens:**
- Aplicação rápida e específica para um elemento
- Alta prioridade (sobrescreve outros estilos)

**Desvantagens:**
- Difícil manutenção
- Código repetitivo
- Mistura conteúdo com apresentação

### 2. CSS Interno (Internal)

O CSS é definido dentro da tag `<style>` no `<head>` do documento HTML.

**Exemplo:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Minha Página</title>
    <style>
        p {
            color: green;
            font-size: 16px;
        }
        h1 {
            color: navy;
            text-align: center;
        }
    </style>
</head>
<body>
    <h1>Título Principal</h1>
    <p>Este é um parágrafo verde.</p>
</body>
</html>
```

**Vantagens:**
- Todos os estilos em um único arquivo
- Útil para páginas únicas

**Desvantagens:**
- Estilos não são reutilizados em outras páginas
- Arquivo HTML fica maior

### 3. CSS Externo (External)

O CSS é escrito em um arquivo separado com extensão `.css` e vinculado ao HTML através da tag `<link>`.

**Arquivo: styles.css**

```css
p {
    color: purple;
    font-size: 16px;
}

h1 {
    color: darkblue;
    text-align: center;
}
```

**Arquivo: index.html**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Minha Página</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Título Principal</h1>
    <p>Este é um parágrafo roxo.</p>
</body>
</html>
```

**Vantagens:**
- Reutilização em múltiplas páginas
- Melhor organização e manutenção
- Separação de conteúdo e apresentação
- Cache do navegador (melhor performance)

**Desvantagens:**
- Requer um arquivo adicional

> **Boa Prática:** Use CSS externo sempre que possível para facilitar a manutenção e reutilização.

---

## Seletores Básicos

Os seletores permitem escolher quais elementos HTML receberão os estilos.

### 1. Seletor de Elemento (Type Selector)

Seleciona todos os elementos de um tipo específico.

**Sintaxe:**

```css
elemento {
    propriedade: valor;
}
```

**Exemplo:**

```css
h1 {
    color: blue;
}

p {
    font-size: 14px;
}

div {
    background-color: lightgray;
}
```

Neste caso, todos os `<h1>`, `<p>` e `<div>` da página receberão esses estilos.

### 2. Seletor de Classe (Class Selector)

Seleciona elementos que possuem um atributo `class` específico. Classes podem ser reutilizadas em múltiplos elementos.

**Sintaxe:**

```css
.nome-da-classe {
    propriedade: valor;
}
```

**Exemplo HTML:**

```html
<p class="destaque">Parágrafo em destaque</p>
<p>Parágrafo normal</p>
<div class="destaque">Div em destaque</div>
```

**Exemplo CSS:**

```css
.destaque {
    color: red;
    font-weight: bold;
}
```

### 3. Seletor de ID (ID Selector)

Seleciona um elemento único que possui um atributo `id` específico. IDs devem ser únicos na página.

**Sintaxe:**

```css
#nome-do-id {
    propriedade: valor;
}
```

**Exemplo HTML:**

```html
<h1 id="titulo-principal">Título Único</h1>
<p id="introducao">Primeiro parágrafo</p>
```

**Exemplo CSS:**

```css
#titulo-principal {
    color: navy;
    text-align: center;
}

#introducao {
    font-size: 18px;
    font-style: italic;
}
```

### 4. Seletor Universal (Universal Selector)

Seleciona todos os elementos da página.

**Sintaxe:**

```css
* {
    propriedade: valor;
}
```

**Exemplo:**

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

Este exemplo remove margens e preenchimentos padrão de todos os elementos.

### Comparação de Seletores

| Seletor | Sintaxe | Exemplo | Uso |
|---------|---------|---------|-----|
| Elemento | `elemento` | `p { }` | Estilizar todos os elementos de um tipo |
| Classe | `.classe` | `.destaque { }` | Estilizar grupos de elementos |
| ID | `#id` | `#header { }` | Estilizar um elemento único |
| Universal | `*` | `* { }` | Estilizar todos os elementos |

---

## Propriedades CSS Básicas

### 1. color

Define a cor do texto.

**Valores possíveis:**
- Nomes de cores: `red`, `blue`, `green`
- Hexadecimal: `#FF0000`, `#00F`, `#336699`
- RGB: `rgb(255, 0, 0)`
- RGBA: `rgba(255, 0, 0, 0.5)` (com transparência)

**Exemplo:**

```css
p {
    color: #333333;
}

.destaque {
    color: rgb(255, 0, 0);
}

#titulo {
    color: darkblue;
}
```

### 2. font-size

Define o tamanho da fonte.

**Valores possíveis:**
- Pixels: `16px`, `20px`
- Ems: `1em`, `1.5em` (relativo ao elemento pai)
- Rems: `1rem`, `1.2rem` (relativo ao elemento raiz)
- Porcentagem: `100%`, `120%`
- Palavras-chave: `small`, `medium`, `large`

**Exemplo:**

```css
body {
    font-size: 16px;
}

h1 {
    font-size: 32px;
}

.pequeno {
    font-size: 12px;
}

.grande {
    font-size: 1.5em;
}
```

### 3. text-align

Define o alinhamento horizontal do texto.

**Valores possíveis:**
- `left`: Alinha à esquerda (padrão)
- `right`: Alinha à direita
- `center`: Centraliza
- `justify`: Justifica

**Exemplo:**

```css
h1 {
    text-align: center;
}

p {
    text-align: justify;
}

.direita {
    text-align: right;
}
```

### Outras Propriedades Úteis

```css
/* Família da fonte */
font-family: Arial, sans-serif;

/* Peso da fonte */
font-weight: bold; /* ou normal, ou valores numéricos 100-900 */

/* Estilo da fonte */
font-style: italic;

/* Cor de fundo */
background-color: #f0f0f0;

/* Margem */
margin: 10px;

/* Preenchimento interno */
padding: 15px;
```

---

## Cascata, Especificidade e Herança

### Cascata

A **cascata** é o mecanismo que determina qual estilo será aplicado quando há múltiplas regras para o mesmo elemento. A ordem importa:

1. **Origem**: Estilos do navegador < Estilos do usuário < Estilos do autor
2. **Importância**: Declarações normais < Declarações `!important`
3. **Especificidade**: (explicado abaixo)
4. **Ordem**: Quando tudo é igual, a última regra vence

**Exemplo:**

```css
p {
    color: blue;
}

p {
    color: red; /* Esta regra vence porque vem depois */
}
```

### Especificidade

A **especificidade** é um peso que determina qual regra CSS é mais importante. Quanto mais específico o seletor, maior seu peso.

**Ordem de especificidade (da menor para a maior):**

1. Seletor universal (`*`) - especificidade: 0
2. Seletores de elemento (`p`, `div`, `h1`) - especificidade: 1
3. Seletores de classe (`.classe`) - especificidade: 10
4. Seletores de ID (`#id`) - especificidade: 100
5. Estilos inline (`style=""`) - especificidade: 1000

**Exemplo:**

```css
/* Especificidade: 1 */
p {
    color: blue;
}

/* Especificidade: 10 - esta regra vence */
.destaque {
    color: red;
}

/* Especificidade: 100 - esta regra vence sobre as anteriores */
#principal {
    color: green;
}
```

**Cálculo de especificidade:**

- `p` = 1
- `.destaque` = 10
- `p.destaque` = 1 + 10 = 11
- `#principal` = 100
- `div#principal.destaque` = 1 + 100 + 10 = 111

### Herança

A **herança** é o mecanismo pelo qual alguns valores de propriedades CSS são transmitidos de elementos pais para elementos filhos.

**Propriedades que são herdadas:**
- `color`
- `font-family`
- `font-size`
- `font-weight`
- `line-height`
- `text-align`

**Propriedades que NÃO são herdadas:**
- `margin`
- `padding`
- `border`
- `background`
- `width`
- `height`

**Exemplo:**

```html
<div style="color: blue; font-size: 16px;">
    <p>Este parágrafo herda a cor azul e o tamanho 16px do div pai.</p>
    <span>Este span também herda os estilos.</span>
</div>
```

**Forçar herança:**

```css
.filho {
    color: inherit; /* Força a herdar a cor do elemento pai */
}
```

---

## Resumo

- **CSS** estiliza páginas HTML, controlando aparência e layout
- **Três formas de aplicar CSS**: inline, interno e externo (prefira externo)
- **Seletores básicos**: elemento, classe (`.`), ID (`#`) e universal (`*`)
- **Propriedades básicas**: `color`, `font-size`, `text-align`
- **Cascata**: Determina qual estilo aplicar quando há conflitos
- **Especificidade**: IDs > Classes > Elementos
- **Herança**: Alguns estilos são passados de pais para filhos automaticamente

---

## Próximos Passos

Agora que você conhece os conceitos fundamentais do CSS, pratique criando e estilizando suas próprias páginas web! Veja os exemplos práticos na pasta `exemplos/` deste repositório.
