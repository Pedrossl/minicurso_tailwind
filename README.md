# Portfólio — Bruna Ribeiro

Projeto de portfólio pessoal desenvolvido como exercício prático do **curso de Tailwind CSS**. O site apresenta a desenvolvedora front-end Bruna Ribeiro, com seções de apresentação, tecnologias, projetos e contato.

---

## Estrutura do Projeto

```
cursoTailwind/
├── src/
│   ├── index.html      # Página principal (Home)
│   ├── sobre.html      # Página Sobre Mim
│   ├── input.css       # CSS de entrada com importação do Tailwind e variáveis customizadas
│   ├── output.css      # CSS gerado pelo Tailwind (não editar manualmente)
│   └── img/            # Imagens do projeto (perfil, projetos, ícones de tecnologias etc.)
├── package.json
└── package-lock.json
```

---

## Páginas

### `index.html` — Home
- **Hero:** apresentação com foto de perfil e chamada para ação
- **Tecnologias:** lista de tecnologias dominadas (HTML5, CSS3, JavaScript, Tailwind CSS) com imagens ilustrativas
- **Projetos:** cards dos projetos realizados com imagem e descrição
- **Contato:** formulário com campos de e-mail e mensagem
- **Footer:** links para redes sociais (LinkedIn, WhatsApp, Gmail, GitHub)

### `sobre.html` — Sobre Mim
- **História:** texto biográfico com trajetória profissional
- **Experiência:** linha do tempo de cargos (estagiária → júnior → pleno → sênior)
- **Formação & Cursos:** graduação e certificações
- **Meus Diferenciais:** destaques como design responsivo, acessibilidade, performance e comunicação

---

## Tecnologias Utilizadas

| Tecnologia | Papel |
|---|---|
| HTML5 | Estrutura semântica das páginas |
| Tailwind CSS v4 | Estilização via classes utilitárias |
| CSS customizado | Variáveis de cor no `input.css` |
| Node.js / npm | Gerenciamento de pacotes e scripts |

---

## Pré-requisitos

- [Node.js](https://nodejs.org/) (v18 ou superior recomendado)
- npm (já incluso com o Node.js)

---

## Instalação

Clone o repositório e instale as dependências:

```bash
git clone <url-do-repositorio>
cd cursoTailwind
npm install
```

---

## Como baixar e usar o Tailwind CSS

Este projeto usa o `@tailwindcss/cli` para gerar o CSS.

1) Instale as dependencias do projeto:

```bash
npm install
```

2) Gere o CSS uma vez (build):

```bash
npm run build
```

3) Ou mantenha o CSS atualizando automaticamente (dev/watch):

```bash
npm run dev
```

Depois disso, abra `src/index.html` (ou `src/sobre.html`) no navegador.

---

## Uso

### Modo desenvolvimento (com watch)

Gera o `output.css` automaticamente sempre que você salvar um arquivo:

```bash
npm run dev
```

Abra `src/index.html` diretamente no navegador (ou use uma extensão como **Live Server** no VS Code).

### Build para produção

Gera o `output.css` uma única vez, com todas as classes utilizadas:

```bash
npm run build
```

> **Atenção:** nunca edite `src/output.css` manualmente — ele é sobrescrito a cada build.

---

## Customização de Cores

As cores do tema estão centralizadas em `src/input.css` como variáveis CSS:

```css
:root {
  --color-primary:           #334155; /* slate-700  — cor principal */
  --color-primary-dark:      #1e293b; /* slate-800  — fundo de cards */
  --color-accent:            #fcd34d; /* amber-300  — destaques */
  --color-text:              #ffffff; /* branco     — texto sobre fundos escuros */
  --color-text-secondary:    #cbd5e1; /* slate-300  — texto secundário */
  --color-text-muted:        #94a3b8; /* slate-400  — texto discreto */
}
```

Para alterar a paleta do site inteiro, basta modificar essas variáveis.

---

## Layout Responsivo

O projeto foi construído com abordagem **mobile-first**. Os breakpoints usados são:

- **Mobile:** layout em coluna única, espaçamentos compactos
- **`md:` (768px+):** layout em linhas, grids com múltiplas colunas, navegação centralizada

---

## Aprendizados do Curso

Este projeto aborda as seguintes práticas do Tailwind CSS:

- Utilidades de layout: `flex`, `grid`, `gap`, `justify-*`, `items-*`
- Responsividade com prefixo `md:`
- Tipografia e cores com classes semânticas do Tailwind
- Customização via variáveis CSS no arquivo de entrada
- Pipeline de build com `@tailwindcss/cli`
