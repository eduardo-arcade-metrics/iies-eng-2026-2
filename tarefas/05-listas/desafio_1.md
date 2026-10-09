# Desafio 1: Tratamento de Dados e Normalização de Sinal

---

## Contexto


sensores frequentemente retornam sinais analógicos ruidosos ou fora de escala que precisam ser filtrados e normalizados no intervalo entre `0.0` e `1.0`.

- **Dados de entrada (sinal do sensor):**  
  `sinais = [12, -5, 45, 102, 88, -12, 60, 110, 35]`

---

## Tarefas

1. Remova qualquer valor inválido (leituras negativas representam falhas de leitura).
2. Ordene a lista filtrada em ordem crescente utilizando o método `.sort()`.
3. Crie uma nova lista com os valores **normalizados** através da fórmula:

$$v_{\text{norm}} = \frac{v - v_{\min}}{v_{\max} - v_{\min}}$$

---
