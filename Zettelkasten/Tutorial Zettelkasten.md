
## Estrutura de Pastas

```

Zettelkasten/

├── Inbox/           # Notas temporárias, ideias iniciais

├── Literatura/      # Notas de referência (livros, artigos)

├── Permanentes/     # Notas permanentes (ideias processadas)

├── Projetos/        # Notas relacionadas a projetos específicos

└── Índices/         # Notas de navegação e mapas de conteúdo

```

  

## Exemplos de Notas

  

### 1. Nota de Literatura (Referência)

```md

# LIT2023021501 Clean Code - Cap 3 - Funções

  

Fonte: Livro "Clean Code" de Robert C. Martin, Capítulo 3

  

## Principais conceitos:

- Funções devem ser pequenas, idealmente com menos de 20 linhas

- Funções devem fazer apenas uma coisa

- Nomes devem ser descritivos e revelar a intenção

- Evitar efeitos colaterais

- Seguir regra de níveis de abstração descendentes

- Limite de argumentos (idealmente menos de 3)

  

#livro #cleancode #boas-práticas #funções

```

  

### 2. Nota Permanente (Conceito)

```md

# 202302151045 Funções Puras

  

Uma função pura é um conceito da programação funcional com duas características principais:

  

1. **Determinismo**: Para as mesmas entradas, sempre retorna os mesmos resultados

2. **Sem efeitos colaterais**: Não modifica estado fora de seu escopo

  

## Exemplo em JavaScript:

```javascript

// Função pura

const somar = (a, b) => a + b;

  

// Função impura (depende de estado externo)

let total = 0;

const somarAoTotal = (valor) => {

  total += valor;

  return total;

};

```

  

## Benefícios:

- Facilidade de teste

- Previsibilidade

- Melhor compreensão do código

- Facilita paralelismo

  

## Links:

[[LIT2023021501 Clean Code - Cap 3 - Funções]]

[[202302151130 Programação Funcional]]

[[202302151210 Imutabilidade em JavaScript]]

  

#programação-funcional #javascript #conceito #boas-práticas

```

  

### 3. Nota Permanente (Problema-Solução)

```md

# 202302151130 Evitando Mutação de Estado em React

  

## Problema:

Atualizar um array de objetos no estado do React sem causar efeitos colaterais indesejados.

  

## Solução:

Usar técnicas de imutabilidade com spread operator ou métodos como map/filter.

  

```jsx

// ❌ Abordagem incorreta (mutação direta)

const adicionarItem = () => {

  const items = state.items;

  items.push({ id: Date.now(), text: novoTexto });

  setState({ items: items });

};

  

// ✅ Abordagem correta (imutável)

const adicionarItem = () => {

  setState({

    items: [...state.items, { id: Date.now(), text: novoTexto }]

  });

};

```

  

## Princípio:

Sempre crie novas referências ao invés de modificar as existentes.

  

## Links:

[[202302151045 Funções Puras]]

[[202302151210 Imutabilidade em JavaScript]]

[[202302151315 Gerenciamento de Estado no React]]

  

#react #imutabilidade #estado #solução-problema

```

  

### 4. Nota Índice (Mapa de Conteúdo)

```md

# MOC - Desenvolvimento Front-end

  

Este mapa de conteúdo conecta tópicos relacionados ao desenvolvimento front-end.

  

## JavaScript

  

### Conceitos Fundamentais

- [[202302150930 Closures em JavaScript]]

- [[202302151045 Funções Puras]]

- [[202302151210 Imutabilidade em JavaScript]]

- [[202302151530 Promises e Async/Await]]

  

### Frameworks

- [[MOC - React]]

- [[MOC - Vue]]

- [[MOC - Angular]]

  

## CSS

- [[202302160845 CSS Grid vs Flexbox]]

- [[202302161230 CSS-in-JS Approaches]]

- [[202302161415 Responsive Design Patterns]]

  

## Performance

- [[202302170920 Técnicas de Lazy Loading]]

- [[202302171045 Web Vitals e Métricas de Performance]]

  

#moc #front-end #mapa-de-conteúdo

```

  

## Fluxo de Trabalho

  

1. **Captura Inicial**: Ao aprender algo novo (ex: assistir uma aula sobre React Hooks)

   - Crie uma nota rápida na pasta "Inbox"

   - Registre os conceitos principais e códigos de exemplo

  

2. **Processamento**: Transforme as notas temporárias em permanentes

   - Crie uma nota permanente para cada conceito individual

   - Ex: Uma nota específica sobre `useEffect`, outra sobre `useState`

   - Use suas próprias palavras, foque no entendimento

  

3. **Conexão**: Vincule a novas e existentes notas

   - Adicione links para notas relacionadas

   - Ex: Conecte `useEffect` com notas sobre lifecycle, side effects, etc.

  

4. **Uso**: Consulte e expanda sua base de conhecimento

   - Use a busca e navegação por links para encontrar soluções

   - Atualize notas existentes com novos insights

  

## Dicas para Programação

  

- Use blocos de código Markdown para exemplos

- Crie notas específicas para padrões e anti-padrões

- Mantenha snippets reutilizáveis para problemas comuns

- Documente erros e suas soluções

- Crie MOCs (Mapas de Conteúdo) para linguagens e frameworks específicos