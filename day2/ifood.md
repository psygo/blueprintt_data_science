# Detecção de Fraudes em Pagamento Online

> Caso de assalto no ato do pagamento. Roubou-se o cartão de crédito e a comida.

O mecanismo de pagamento digital é hoje uma spinoff, Fintech, MovilePay.

iFood oferece também:

- iFood shop para os restaurantes a partir dos créditos.
- Também oferece adiantamento de pagamento sob uma pequena taxa.

Fraudadores utilizavam contas do iFood para fazer transações, não exatamente os cartões roubados.

*Há uma opção sempre para receber o dinheiro de volta, para evitar fraudes.*

No caso, o iFood sempre toma o prejuízo, apesar de que a fraude não necessariamente aconteceu no iFood. Seria possível fazer uma operação de *charge back* ou *esputa*, mas isso seria muito burocrático e não escalável.

iFood muitas vezes é testado para testar se o cartão clonado é *quente*.

Se houver 5% de comissão, serão precisas 20 vendas para compensar 1 fraude.

## Estrutura de Segurança

Inicialmente, havia um *motor de regras* no backend. Mas era muito lento e conservador. Então flexibilizou-se o processo e terceirizou-se as dúvidas para empresas de segurança.

Então, começou-se a colocar Machine Learning no backend.

## Problemas de Machine Learning

Há uma percentagem muito pequena de fraudes, as classes são muito desbalanceadas. A curva de ROC também não funciona muito bem.

### Correspondência da Matriz de Confusão para o Negócio

TP = + valor taxa
TN = + valor pedido
FP e FN = - valor do pedido

Com isso, pode-se obter o valor ótimo para o *threshold*.

## Implementação de ML

Felizmente, o iFood tem uma plataforma para implementação de modelos no aplicativo, chamada *Alfred*.

Dataprep:

- databricks
- Spark ML

Endpoint:

- mleap

*Alfred* facilida a modificação do modelo no backend para mais fácil implementação.

A plataforma *Alfred* foi criada independentemente (e antes) de demandas específicas.