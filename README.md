# CalcLazy — Rebalanceamento Lazy Ótimo

Calculadora de rebalanceamento de carteira baseada na técnica **Optimal Lazy Rebalancing**, originalmente descrita e implementada por Albert H. Mao.

---

## O que é o rebalanceamento lazy?

A ideia central é simples: **rebalanceie a carteira somente quando houver aporte ou resgate**.

- Ao **aportar**, compre apenas os ativos abaixo do alvo, usando o valor aportado para se aproximar ao máximo da alocação desejada, sem vender nada.
- Ao **resgatar**, venda apenas os ativos acima do alvo, obtendo o valor desejado enquanto se aproxima da alocação alvo, sem comprar nada.

Isso evita tributação desnecessária sobre ganhos de capital, reduz custos de transação e minimiza a quantidade de operações. O algoritmo encontra a distribuição ótima do aporte/resgate entre os ativos elegíveis — não é uma estimativa visual, é o cálculo exato.

---

## Funcionalidades

- **Cálculo lazy ótimo** — algoritmo de preenchimento por nível d'água (water-level fill) que distribui aportes e resgates minimizando desvios sem cruzar operações
- **Mínimo de movimentação por ativo** — respeita o valor mínimo de cada fundo; ativos abaixo do mínimo são excluídos e o valor é redistribuído
- **Sem servidor** — aplicação single-file HTML + JS puro, hospedável no GitHub Pages sem nenhum backend
- **Organização de ativos** — arraste e solte para reordenar linhas
- **Filtro por tags** — agrupe ativos por categoria e filtre a visualização; totais do rodapé se ajustam ao filtro
- **Visibilidade de colunas** — escolha quais colunas exibir via menu "Colunas ▾"
- **Redimensionamento de colunas** — arraste a borda de qualquer coluna para ajustar a largura
- **CNPJ** — campo dedicado com formatação automática `XX.XXX.XXX/XXXX-XX`
- **Aplicar rebalanceamento** — soma os valores calculados de Comprar/Vender ao saldo atual de cada ativo com um clique; desfazível na mesma sessão
- **Ordem de movimentação** — pop-up com a lista de ativos a comprar/vender (CNPJ · Nome · Valor) com botão de cópia
- **Histórico gráfico** — salve snapshots manuais da carteira e visualize a evolução do patrimônio total e de cada ativo em gráficos de linha (um ponto por dia)

---

## Como usar

### Primeiro acesso

1. Crie um **Personal Access Token (PAT)** no GitHub com permissão `Contents: read & write` no repositório
2. Acesse o app pelo GitHub Pages do repositório
3. Defina uma senha forte e cole o token — a carteira cifrada é criada automaticamente no repositório

---

## Tecnologias

| Camada | Tecnologia |
|--------|-----------|
| Interface | HTML + CSS + JavaScript |
| Criptografia |
| Persistência | GitHub Contents API |
| Gráficos |
| Fontes | Google Fonts (Space Grotesk · JetBrains Mono) |

---

## Créditos

Algoritmo original de rebalanceamento lazy por **Albert H. Mao** — licença GPL 3.
