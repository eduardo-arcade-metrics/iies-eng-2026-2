# Desafio 2: Análise de Peças em Estoque (Listas Aninhadas)

---

## Contexto

É comum gerenciar matrizes ou tabelas de dados onde cada linha representa uma peça e suas propriedades.

- **Estrutura de cada linha:** `[ID_Peca, Quantidade, Preco_Unitario_R$]`

```python
estoque = [
    [101, 50, 12.50],
    [102, 120, 4.00],
    [103, 15, 150.00],
    [104, 80, 25.00]
]
```

---

## Tarefa

1. Calcule o valor total imobilizado no estoque (soma de $\text{Quantidade} \times \text{Preço Unitário}$ para todos os itens).
2. Identifique e exiba o `ID_Peca` do item com o maior valor total investido individualmente.

---

