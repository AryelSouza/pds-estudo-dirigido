# Parte 4 – Projeto de Filtros FIR

## Introdução

Filtros FIR (Finite Impulse Response) são filtros com resposta ao impulso finita, ou seja, a saída depende apenas das entradas atuais e passadas, não das saídas passadas. Eles são sempre estáveis e podem ser projetados para ter fase linear.

## Características dos Filtros FIR

- Sempre estáveis
- Fase linear (possível)
- Implementação simples
- Requerem mais coeficientes do que filtros IIR para desempenho equivalente

## Equação de Diferença

\[
y[n] = \sum_{k=0}^{M} b_k \cdot x[n-k]
\]

## Métodos de Projeto

- **Janela de tempo:** define uma resposta ideal e a multiplica por uma janela (Hamming, Blackman, etc.)
- **Parks-McClellan:** algoritmo otimizado (equiripple)
- **Kaiser window:** parametrizável, boa flexibilidade

## Implementação com `scipy.signal.firwin`

Exemplo de filtro passa-baixas com janela de Hamming:

```python
b = signal.firwin(numtaps=51, cutoff=0.3, window="hamming")
