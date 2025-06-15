# Parte 5 – Projeto de Filtros IIR

## Introdução

Filtros IIR (Infinite Impulse Response) possuem resposta ao impulso infinita e são implementados usando realimentação (feedback). São mais eficientes que filtros FIR em termos de número de coeficientes, mas exigem cuidado com estabilidade e fase.

## Características

- Resposta ao impulso infinita
- Utilizam entradas e saídas passadas
- Podem ser instáveis
- Normalmente têm fase não-linear
- Mais eficientes que filtros FIR

## Tipos Comuns de Filtros IIR

- **Butterworth:** resposta suave, sem ondulações
- **Chebyshev Tipo I:** ondulação na banda passante
- **Chebyshev Tipo II:** ondulação na banda de rejeição
- **Elíptico (Cauer):** ondulações em ambas as bandas, mais eficiente

## Etapas do Projeto

1. Especificar requisitos (frequência de corte, atenuação, ripple, etc.)
2. Usar `scipy.signal.butter`, `cheby1`, `ellip`, etc.
3. Obter coeficientes do filtro
4. Aplicar com `lfilter` ou `filtfilt` (com correção de fase)

## Exemplo de filtro Butterworth com `scipy`

```python
b, a = signal.butter(order, cutoff, btype='low', fs=fs)
