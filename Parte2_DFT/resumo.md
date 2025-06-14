# Parte 2 – Transformada Discreta de Fourier (DFT)

## Introdução

A Transformada Discreta de Fourier (DFT) é uma das ferramentas mais importantes do Processamento Digital de Sinais. Ela converte um sinal no tempo discreto e finito para o domínio da frequência, permitindo a análise espectral de sinais.

## Definição Matemática

A DFT de um sinal \( x[n] \) de comprimento \( N \) é definida por:

\[
X[k] = \sum_{n=0}^{N-1} x[n] \cdot e^{-j2\pi kn/N}, \quad k = 0, 1, ..., N-1
\]

A transformada inversa é:

\[
x[n] = \frac{1}{N} \sum_{k=0}^{N-1} X[k] \cdot e^{j2\pi kn/N}
\]

## Propriedades Importantes

- Periodicidade: \( X[k + N] = X[k] \)
- Linearidade
- Simetria
- Convolução circular
- Dualidade

## Relação com a FFT

A **Fast Fourier Transform (FFT)** é um algoritmo eficiente para calcular a DFT. Reduz a complexidade de \( O(N^2) \) para \( O(N \log N) \).

## Aplicações

- Análise espectral
- Compressão de sinais
- Processamento de áudio e imagens
- Comunicações digitais
