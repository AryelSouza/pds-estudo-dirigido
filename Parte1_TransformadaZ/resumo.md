# Parte 1 – A Transformada-Z

## Definição
A Transformada-Z é uma ferramenta fundamental na análise e projeto de sistemas discretos. Ela representa sinais no domínio da frequência complexa, permitindo estudar a estabilidade e resposta de sistemas lineares invariantes no tempo (LTI).

## Forma Geral
A transformada-z de um sinal discreto \( x[n] \) é dada por:

\[
X(z) = \sum_{n=-\infty}^{\infty} x[n] \cdot z^{-n}
\]

## Região de Convergência (ROC)
A ROC é o conjunto de valores de \( z \) para os quais a série converge. A ROC determina se a transformada-z existe e se o sistema é causal ou estável.

## Propriedades Importantes
- Linearidade
- Deslocamento no tempo
- Convolução
- Derivada
- Inicial e final value theorems

## Utilidade
- Estudo da estabilidade de filtros
- Projeto de sistemas digitais
- Análise de sistemas no domínio da frequência
