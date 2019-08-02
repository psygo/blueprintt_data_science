# Dados Internos - Como extrair valor para o Negócio?

> Ninguém tem mais dados do que uma empresa de telecomunicações. Serviços como Google têm seus dados passando pela infraestrutura das empresas de telecomunicações.

A Claro possui a NET, portanto o maior número de assinaturas.

Para tentar evitar cair na onda de *must have* do ML, tentou-se especificar as necessidades do negócio antes de se comprometer. (O gráfico respectivo é bastante instrutivo.) Também é preciso especificar bem as pessoas necessárias, pois unicórnios são impossíveis de se achar.

Cita-se um caso da Maria, que não possui crédito bancário, mas possui renda. O problema é que os bancos não têm informação para fornecer crédito, porém a Claro tem.

# Avaliação de Crédito

A área de vendas e a área de inadimplência brigam pelo *threshold* de aprovação de vendas.

Pessoas de baixa renda, que compõem a maior parte do setor de rentabilização, deixam pouca informação. Muito devido a esse setor, 30% das vendas são rejeitadas.

Criou-se então um *Claro Score*, o que também diminuiu a dependência de Bureaus de Crédito, reduzindo custos. No final, depois de muitas iterações e ajuda dos modelos do Bureau, chegou-se a 37% de ROC-AUC , o que levou a 16% de redução da inadimplência, 876% ROI nos primeiros 24 meses. Esse produto acabou passando a ser revendido para outras empresas também.

# Implementação

Foram 6 meses para a implementação do Claro Score.

Em geral, na Claro, colocam-se uma equipe de Piloto e de Controle, porém, como nesse caso o modelo anterior era muito ruim, optou-se por uma estratégia mais *kamikaze*.