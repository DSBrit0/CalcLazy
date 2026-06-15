# CalcLazy — Rebalanceamento Lazy Ótimo

Calculadora de rebalanceamento de carteira baseada na técnica **Optimal Lazy Rebalancing**, originalmente descrita e implementada por Albert H. Mao.

---

## O que é o rebalanceamento lazy?

A ideia central é simples: **rebalanceie a carteira somente quando houver aporte ou resgate**.

- Ao **aportar**, compre apenas os ativos abaixo do alvo, usando o valor aportado para se aproximar ao máximo da alocação desejada, sem vender nada.
- Ao **resgatar**, venda apenas os ativos acima do alvo, obtendo o valor desejado enquanto se aproxima da alocação alvo, sem comprar nada.

Isso evita tributação desnecessária sobre ganhos de capital, reduz custos de transação e minimiza a quantidade de operações. O algoritmo encontra a distribuição ótima do aporte/resgate entre os ativos elegíveis — não é uma estimativa visual, é o cálculo exato.
