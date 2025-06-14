# Parte 1 – A Transformada-Z

## Introdução

A transformada-z é uma das ferramentas mais importantes na análise de sistemas lineares discretos no tempo. Assim como a transformada de Laplace é usada em sistemas contínuos, a transformada-z permite representar e manipular sinais no domínio da frequência complexa.

## Definição

A transformada-z de uma sequência \( x[n] \) é definida por:

\[
X(z) = \sum_{n=-\infty}^{\infty} x[n] \cdot z^{-n}
\]

onde \( z \in \mathbb{C} \) é uma variável complexa.

## Região de Convergência (ROC)

A série só converge para certos valores de \( z \), que formam a chamada região de convergência (ROC). Essa região determina:
- Causalidade
- Estabilidade
- Existência da transformada

## Propriedades Importantes

- **Linearidade:** A[z]{a·x[n] + b·y[n]} = a·X(z) + b·Y(z)
- **Deslocamento no tempo:** A[z]{x[n - k]} = z⁻ᵏ·X(z)
- **Convolução no tempo:** A[z]{x[n] * h[n]} = X(z)·H(z)
- **Valor inicial:** \( x[0] = \lim_{z \to \infty} X(z) \)
- **Valor final:** \( x[\infty] = \lim_{z \to 1} (1 - z^{-1})X(z) \), se existir

## Aplicações

- Análise de estabilidade e resposta de sistemas LTI
- Projeto e implementação de filtros digitais
- Transformações de domínio de sinais
