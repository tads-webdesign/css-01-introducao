# Exemplos Práticos - Introdução ao CSS

Esta pasta contém exemplos práticos demonstrando os conceitos fundamentais de CSS apresentados no tutorial.

## Arquivos de Exemplo

### 1. CSS Inline (`01-inline.html`)
Demonstra como aplicar CSS diretamente nos elementos HTML usando o atributo `style`.

**Características:**
- Estilos aplicados diretamente em cada elemento
- Alta especificidade
- Útil para estilos únicos e específicos

**Para visualizar:**
Abra o arquivo `01-inline.html` em seu navegador.

### 2. CSS Interno (`02-interno.html`)
Demonstra como definir CSS dentro da tag `<style>` no `<head>` do documento.

**Características:**
- Estilos centralizados no mesmo arquivo HTML
- Uso de seletores (elemento, classe, ID)
- Melhor organização que inline

**Para visualizar:**
Abra o arquivo `02-interno.html` em seu navegador.

### 3. CSS Externo (`03-externo.html` + `styles.css`)
Demonstra a forma recomendada de aplicar CSS: arquivo externo vinculado ao HTML.

**Características:**
- Separação completa entre conteúdo (HTML) e apresentação (CSS)
- Reutilizável em múltiplas páginas
- Melhor manutenção e organização
- Exemplos de todos os tipos de seletores

**Para visualizar:**
Abra o arquivo `03-externo.html` em seu navegador. O arquivo `styles.css` será carregado automaticamente.

## Conceitos Demonstrados

Todos os exemplos demonstram:

### ✅ Tags HTML
- `<h1>` a `<h6>`: Títulos de diferentes níveis
- `<p>`: Parágrafos
- `<div>`: Containers de bloco
- `<span>`: Containers inline

### ✅ Seletores CSS
- **Elemento**: `h1`, `p`, `div`
- **Classe**: `.secao`, `.texto-centralizado`, `.botao`
- **ID**: `#cabecalho`, `#rodape`, `#cta`
- **Universal**: `*` (no exemplo externo)

### ✅ Propriedades CSS
- `color`: Cor do texto
- `font-size`: Tamanho da fonte
- `text-align`: Alinhamento do texto (left, center, right, justify)
- `background-color`: Cor de fundo
- `padding`: Espaçamento interno
- `margin`: Espaçamento externo
- `font-weight`: Peso da fonte
- `font-style`: Estilo da fonte (italic)

### ✅ Conceitos Avançados
- **Cascata**: Ordem de aplicação dos estilos
- **Especificidade**: ID > Classe > Elemento
- **Herança**: Propriedades que passam de pai para filho

## Como Usar os Exemplos

1. **Explore o código**: Abra cada arquivo em um editor de texto para ver como o CSS está estruturado
2. **Visualize no navegador**: Abra os arquivos HTML no navegador para ver o resultado
3. **Experimente**: Modifique os valores das propriedades CSS e recarregue a página para ver as mudanças
4. **Compare**: Veja as diferenças entre as três formas de aplicar CSS

## Exercícios Práticos

### Exercício 1: Modificar Cores
Altere as cores dos títulos e parágrafos em cada exemplo para cores diferentes.

### Exercício 2: Ajustar Tamanhos
Modifique os tamanhos de fonte (`font-size`) e veja como isso afeta a hierarquia visual.

### Exercício 3: Criar Novas Classes
No exemplo externo, crie uma nova classe CSS e aplique-a a um elemento HTML.

### Exercício 4: Experimentar com Especificidade
No arquivo `03-externo.html`, adicione um novo parágrafo com:
- Apenas seletor de elemento
- Com uma classe
- Com um ID

Compare como a especificidade afeta a cor final do texto.

### Exercício 5: Testar Herança
Crie um `<div>` com estilos de cor e fonte, e adicione vários elementos filhos (`<p>`, `<span>`) dentro dele. Observe quais propriedades são herdadas.

## Dicas

- Use o **DevTools** do navegador (F12) para inspecionar elementos e ver quais estilos estão sendo aplicados
- Experimente valores diferentes para entender melhor como cada propriedade funciona
- Prefira sempre **CSS externo** para projetos reais
- Mantenha seus seletores **simples e específicos**
- Use **classes** para estilos reutilizáveis e **IDs** para elementos únicos

## Próximos Passos

Depois de explorar estes exemplos, você pode:
1. Criar sua própria landing page do zero
2. Experimentar com mais propriedades CSS (border, box-shadow, transform, etc.)
3. Aprender sobre CSS Grid e Flexbox para layouts avançados
4. Estudar CSS responsivo com media queries

---

Volte ao [Tutorial Principal](../tutorial.md) para revisar os conceitos.
