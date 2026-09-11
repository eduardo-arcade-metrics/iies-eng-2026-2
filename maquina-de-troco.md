# Atividade — Máquina de Troco

## Parte 1 — Descrição narrativa

A máquina começa solicitando ao cliente o preço do produto e o valor pago. 
Os valores são trabalhados em centavos para evitar erros de arredondamento.

Primeiramente, a máquina verifica se o valor pago é menor que o preço do 
produto. Se for menor, a máquina exibe a mensagem "Valor insuficiente" e 
encerra o processo.

Se o valor pago for igual ao preço do produto, a máquina exibe a mensagem 
"Sem troco" e encerra o processo.

Caso o valor pago seja maior que o preço, a máquina calcula o troco 
subtraindo o preço do valor pago.

Depois disso, a máquina verifica as cédulas e moedas disponíveis em ordem 
decrescente de valor. Para cada valor, calcula quantas unidades podem ser 
devolvidas utilizando a divisão inteira DIV. Em seguida, utiliza MOD para 
calcular o restante do troco.

O processo continua passando por todas as cédulas e moedas disponíveis até 
que o valor restante do troco seja igual a zero. Quando isso acontece, a 
máquina encerra o processo.

## Parte 2 — Fluxograma

```mermaid
flowchart TD
    A([INÍCIO]) --> B[/Ler preço do produto e valor pago/]
    B --> C{Valor pago < preço?}

    C -- SIM --> D[/Exibir "Valor insuficiente"/]
    D --> Z([FIM])

    C -- NÃO --> E[Calcular troco = valor pago - preço]
    E --> F{Troco = 0?}

    F -- SIM --> G[/Exibir "Sem troco"/]
    G --> Z

    F -- NÃO --> H[Inicializar lista de cédulas e moedas em ordem decrescente]
    H --> I[Selecionar próximo valor da lista]
    I --> J[quantidade = troco DIV valor]
    J --> K{Quantidade > 0?}

    K -- SIM --> L[/Exibir quantidade de cédulas/moedas e seu valor/]
    L --> M[troco = troco MOD valor]
    M --> N{Existem mais valores na lista?}

    K -- NÃO --> N

    N -- SIM --> I
    N -- NÃO --> Z([FIM])

## Parte 3 — Pseudocódigo

```text
ALGORITMO maquina_de_troco

    LEIA preco
    LEIA pago

    preco ← preco * 100
    pago ← pago * 100

    SE pago < preco ENTÃO

        ESCREVA "Valor insuficiente"

    SENÃO

        troco ← pago - preco

        SE troco = 0 ENTÃO

            ESCREVA "Sem troco"

        SENÃO

            valores ← [10000, 5000, 2000, 1000, 500, 200,
                       100, 50, 25, 10, 5, 1]

            PARA CADA valor EM valores FAÇA

                quantidade ← troco DIV valor

                SE quantidade > 0 ENTÃO

                    ESCREVA quantidade, " x ", valor

                    troco ← troco MOD valor

                FIM SE

            FIM PARA

        FIM SE

    FIM SE

FIM ALGORITMO
```


servem para fazer o GitHub mostrar o pseudocódigo em uma caixa.

# ETAPA 13 — Colocar os testes

Depois do pseudocódigo:

```markdown
## Exemplos de testes

| Preço | Pago | Resultado |
|---|---|---|
| R$ 3,50 | R$ 2,00 | Valor insuficiente |
| R$ 5,00 | R$ 5,00 | Sem troco |
| R$ 3,50 | R$ 5,00 | 1 × R$ 1,00 + 1 × R$ 0,50 |
| R$ 7,30 | R$ 10,00 | 1 × R$ 2,00 + 1 × R$ 0,50 + 2 × R$ 0,10 |

## Comparação das três representações

A descrição narrativa foi a mais fácil de escrever, pois permite explicar 
o funcionamento do sistema usando palavras simples.

O fluxograma facilita a visualização do processo, principalmente das 
decisões e repetições.

O pseudocódigo foi a representação mais precisa, pois mostra claramente 
as entradas, decisões, cálculos e repetições, facilitando a implementação 
do sistema em uma linguagem de programação.
