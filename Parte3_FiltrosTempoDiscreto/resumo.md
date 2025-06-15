# Parte 3 – Implementação de Filtros Discretos no Tempo

## Introdução

Filtros digitais são fundamentais no processamento de sinais. Eles podem ser usados para remover ruídos, extrair frequências específicas, suavizar sinais, entre outros. Os filtros são implementados com equações de diferença no domínio discreto.

## Classificação dos Filtros

- **FIR (Finite Impulse Response):** Resposta ao impulso finita. Depende apenas de entradas passadas.
- **IIR (Infinite Impulse Response):** Resposta ao impulso infinita. Depende de entradas e saídas passadas.

## Forma Geral da Equação de Diferença

\[
y[n] = \sum_{k=0}^{M} b_k x[n-k] - \sum_{k=1}^{N} a_k y[n-k]
\]

- \( b_k \): coeficientes do numerador (parte FIR)
- \( a_k \): coeficientes do denominador (parte IIR)
- \( x[n] \): entrada
- \( y[n] \): saída

## Implementação com `lfilter`

A função `scipy.signal.lfilter(b, a, x)` implementa essa equação diretamente:
- `b`: coeficientes do numerador
- `a`: coeficientes do denominador
- `x`: sinal de entrada

## Aplicações

- Remoção de ruído
- Equalização
- Detecção de bordas em imagens
- Processamento de áudio e voz
