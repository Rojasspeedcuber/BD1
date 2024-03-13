### BD1
Entidades:

Cliente

ID_Cliente (chave primária)
Nome
Email
Endereço
Telefone
Produto

ID_Produto (chave primária)
Nome
Descrição
Preço
Quantidade em estoque
Pedido

ID_Pedido (chave primária)
Data do Pedido
Status do Pedido (em processamento, enviado, entregue, cancelado)
Pagamento

ID_Pagamento (chave primária)
Método de Pagamento (cartão de crédito, boleto, transferência bancária)
Data do Pagamento
Valor Pago
Relacionamentos e Cardinalidades:

Cliente realiza Pedido (1:N)

Um Cliente pode fazer vários Pedidos, mas cada Pedido é feito por um único Cliente.
Pedido tem Pagamento (1:1)

Um Pedido é associado a um único Pagamento, mas um Pagamento está associado a apenas um Pedido.
Agregação:

Pedido inclui Produto (1:N)
Um Pedido pode incluir vários Produtos, e um Produto pode estar em vários Pedidos.
Este relacionamento de agregação é representado dentro da entidade Pedido, incluindo os detalhes dos produtos no pedido:
ID_Pedido (chave primária)
ID_Produto (chave estrangeira referenciando Produto)
Quantidade