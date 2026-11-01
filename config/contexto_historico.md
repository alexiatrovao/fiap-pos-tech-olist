# Contexto de negócio e evidências históricas — NÃO é System Prompt

Origem: **Relatório Executivo Olist**, análises do Brazilian E-Commerce Public Dataset by Olist, aproximadamente set/2016–out/2018 (99.441 pedidos no conjunto completo). O conjunto **não** deve ser interpretado como operação atual ou sistemas online.

## Logistics
- Entre 96.476 pedidos com datas de entrega e previsão, **6,77%** tiveram entrega após a data prevista (comparação por dia calendário).
- Nota média: antecipado **4,29**; exatamente na data **4,03**; até 5 dias de atraso **2,99**; 6–10 dias **1,77**; acima de 10 dias **1,71**.
- Em recorte de pedidos com reviews: mediana de preparação **3,07 dias** atrasados versus **1,79** no prazo; mediana de transporte **26,11** versus **6,94 dias**.
- O dataset não identifica transportadoras individuais; não há acompanhamento em tempo real dos envios.

## Voice of Customer
- Entre avaliações negativas com comentários, atraso/entrega/demora é o conjunto de termos mais mencionado nas análises por palavras-chave; também aparecem produto errado/incompleto, atendimento e defeito.
- Dentre avaliações negativas que mencionam atendimento **em pedidos atrasados**, **59,13%** também mencionam entrega.
- Essas categorias se baseiam em palavras-chave e comentários escritos, **não** em uma avaliação completa de classificação semântica. A seção específica do Problema 2 no relatório não detalha novos indicadores quantitativos.

## Customer Service & Engagement
- Agrupando por identificador único do cliente, **96,9%** compraram uma vez e **3,1%** repetiram a compra no intervalo analisado.
- Entre avaliações de clientes de compra única, **77,0%** foram positivas (4–5), **14,7%** negativas (1–2) e **8,2%** neutras (3).
- Avaliações textuais que mencionam atendimento: nota média **2,56** contra **3,73** nas que não mencionam. Destas avaliações com menção ao atendimento, **56,7%** são negativas.
- Dados são anonimizados; não há histórico completo de SAC nem dados suficientes de consentimento e contatos para campanhas.

## Regras de aplicação
1. Use estas informações só como **hipóteses e motivação de negócio** no modo `historical_analysis` ou em texto de apresentação; jamais emita um alerta atual a partir delas.
2. Não trate médias históricas como thresholds automáticos ou validação de hipóteses causais.
3. Identifique sempre fonte, janela, população, metodologia e limitações da análise antes de citar estatísticas.
