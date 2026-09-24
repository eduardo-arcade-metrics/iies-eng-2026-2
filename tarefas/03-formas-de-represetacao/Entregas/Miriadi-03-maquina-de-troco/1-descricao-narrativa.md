# Descrição Narrativa — Máquina de Troco

A máquina de autoatendimento recebe o preço do produto e o valor pago pelo cliente.

Primeiramente, a máquina verifica se o valor pago é suficiente para comprar o produto. Se o valor pago for menor que o preço, a máquina informa que o valor é insuficiente e encerra o processo.

Se o valor pago for igual ao preço do produto, a máquina informa que não há troco e encerra o processo.

Quando o valor pago for maior que o preço, a máquina calcula o valor do troco, subtraindo o preço do produto do valor pago.

Em seguida, a máquina verifica as cédulas e moedas disponíveis, começando pelo maior valor. Para cada valor disponível, ela calcula quantas unidades podem ser utilizadas no troco e atualiza o valor restante.

A máquina continua esse processo até que todo o troco seja devolvido. Ao final, exibe a quantidade de cada cédula e moeda que deve ser entregue ao cliente e encerra o processo.
