# Tarefa 33: página pessoal com DaisyUI

Página pessoal de uma única tela rolável, feita só com `index.html`, Tailwind 4 e DaisyUI 5 via CDN, sem JavaScript.

## Componentes DaisyUI utilizados

| Componente | Onde aparece |
|---|---|
| `navbar` | Topo da página, com marca, links e botão de contato |
| `dropdown` + `menu` | Menu de navegação no celular e links do navbar no desktop |
| `hero` | Bloco de abertura com nome, área de atuação e botões |
| `avatar` (placeholder) | Iniciais em círculo no hero |
| `btn` | `btn-primary`, `btn-outline` e `btn-ghost` no hero, nos cards e no formulário |
| `badge` | `badge-primary`, `badge-secondary`, `badge-accent`, `badge-outline` e `badge-ghost` na apresentação e nos cards |
| `card` (`card-body`, `card-title`, `card-actions`) | Três projetos e o formulário |
| `input`, `textarea`, `fieldset`, `label` | Formulário de contato |
| `alert` (`alert-info alert-soft`) | Outras formas de contato |
| `toggle` + `theme-controller` | Troca entre os temas `nord` e `dracula` |
| `footer` | Rodapé |

## Por que navbar e hero juntos

Usei os dois porque fazem trabalhos diferentes. O `navbar` fica fixo no topo e permite ir a qualquer seção a qualquer momento. O `hero` ocupa a primeira tela e apresenta quem eu sou e o que faço, com os dois botões principais. Só com o navbar, a página abriria sem apresentação; só com o hero, o visitante perderia a navegação ao rolar.

## Pontos de ajuste com Tailwind

1. **Navbar fixo com desfoque:** o `navbar` do DaisyUI não vem fixo. Acrescentei `sticky top-0 z-20 bg-base-100/85 backdrop-blur` para ele acompanhar a rolagem sem esconder o conteúdo por trás.
2. **Grade dos cards:** o `card` descreve um único cartão, não a disposição de vários. A grade responsiva (`grid md:grid-cols-2 lg:grid-cols-3`) e a altura igual (`h-full`) vêm do Tailwind.

Também usei `scroll-mt-20` nas seções para o título não ficar embaixo do navbar ao clicar num link.

## Reflexão sobre temas

Testei `nord` (claro) e `dracula` (escuro), alternando pelo toggle do navbar e também pelo atributo `data-theme` no DevTools.

> Complete com a sua opinião depois de abrir a página nos dois temas: qual ficou mais coerente com o seu conteúdo e por quê? Comente contraste dos badges, dos botões `outline` e do alerta.

## Como rodar

Abra o `index.html` no navegador. É preciso internet para carregar Tailwind, DaisyUI e a fonte.
