# Como estamos integrando e trazendo inteligência para o app do GuiaBolso

Estrutura parecida com o iFood.

*Data Driven Decisions, not Experienced Based Decisions.*

**OLTP vs OLAP**.

## Arquitetura

No passado, backend em Amazon Redshift e Excel + R.

Depois, foi preciso passar para Spark, mas a manutenção era bastante custosa operacionalmente.

**DataBricks** automatiza a manutenção do ApacheSpark.

Também se utilizam agora grafos para armazenamento de dados atualmente.

`looker` é melhor do que o `tableau` para exploração dos dados.

Volume de dados: 4,5 mi de usuários; 1,2 bi de transações.

Consegue-se utilizar muita computação agressiva e autoscaling agressivo de clusters.

`Parquet` facilita o acesso a features específicas no DB relacional.

Há também *Data Anomaly Detection*.

`mleap` é excelente para utilizar o modelo em tempo real. Porém ele é limitado em relação aos modelos quee ele disponibiliza.

Dentro do AWS, mudou-se para o `lambda`.

## Use Case : Credit Scoring

Já antigo no GuiaBolso.

## Use Case : Classificação de Compras

Categoriza-se em restaurantes, compras de dia a dia, etc, com o modelo clássico de *TF-IDF*.

## Integração do AI com o Backend ML

Criação automatizada de variáveis.

Pode virar:

- API
- modelo para o `mleap`
- ou mesmo uma *simples regra*

Paralelização dos processos e autoscaling no AWS.

## Integração do Backend com o Usuário

Foi preciso ensinar tecnicamente o que estava acontecendo.

*Só é inteligente se parece inteligente* (ambos em termos superficiais e efetivos).

Implementou-se uma maneira de receber *feedback* do usuário, que vão retroalimentando os seus sinais.

**Coletar eventos** é imprescindível para se obter *dados* e *feedback* do usuário.

## Outras Informações

GuiaBolso foi selecionado para programa global de aceleraçãdo do Google, no Vale do Silício.