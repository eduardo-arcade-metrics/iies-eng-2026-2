# Fluxograma — Máquina de Troco

```mermaid
flowchart TD
    A([Início]) --> B[/Ler preço e valor pago/]
    B --> C{Valor pago é suficiente?}
    C -- Não --> D[/Exibir "Valor insuficiente"/]
    D --> E([Fim])
    C -- Sim --> F{Valor pago é igual ao preço?}
    F -- Sim --> G[/Exibir "Sem troco"/]
    G --> E
    F -- Não --> H[Calcular troco]
    H --> I[Percorrer valores das cédulas e moedas em ordem decrescente]
    I --> J[Calcular quantidade de cada valor]
    J --> K[/Exibir quantidade de cada cédula/moeda/]
    K --> E
