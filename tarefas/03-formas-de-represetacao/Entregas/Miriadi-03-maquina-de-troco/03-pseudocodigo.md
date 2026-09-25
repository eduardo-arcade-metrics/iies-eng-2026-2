# Pseudocódigo — Máquina de Troco

ALGORITMO maquina_de_troco

    LEIA preco, pago

    SE pago < preco ENTÃO
        ESCREVA "Valor insuficiente"
    SENÃO

        troco ← pago - preco

        SE troco = 0 ENTÃO
            ESCREVA "Sem troco"
        SENÃO

            PARA CADA valor EM [10000, 5000, 2000, 1000, 500, 200, 100, 50, 25, 10, 5, 1] FAÇA

                quantidade ← troco DIV valor
                troco ← troco MOD valor

                SE quantidade > 0 ENTÃO
                    ESCREVA quantidade, " unidade(s) de R$", valor / 100
                FIM SE

            FIM PARA

        FIM SE

    FIM SE

FIM ALGORITMO
