## Critérios de Classificação

As imagens do dataset foram classificadas em três classes de qualidade estrutural: `GOOD`, `FAIR` e `POOR`. A rotulagem foi baseada na inspeção visual dos defeitos presentes nos dormentes, considerando critérios técnicos associados à presença de trincas, exposição de armadura, deformações e comprometimento estrutural.

A classificação seguiu uma lógica conservadora: quando uma imagem apresentava características próximas ao limite entre duas classes, foi adotada a classe de maior severidade, priorizando a segurança operacional.

### Classes

| Classe | Descrição geral |
|---|---|
| `GOOD` | Dormente em boas condições, sem defeitos estruturais relevantes. |
| `FAIR` | Dormente com deterioração moderada, exigindo monitoramento ou substituição em médio prazo. |
| `POOR` | Dormente com deterioração severa, indicando necessidade de substituição em curto prazo. |

### Critérios utilizados

| Critério | `GOOD` | `FAIR` | `POOR` |
|---|---|---|---|
| Trincas longitudinais | Ausentes ou microfissuras superficiais | Entre 0,5 mm e 1,5 mm | Maiores que 1,5 mm ou com penetração significativa |
| Trincas transversais/oblíquas | Ausentes | Propagação entre 1/3 e 2/3 da altura da seção | Propagação superior a 2/3 da altura ou fratura completa |
| Armadura exposta | Não aparente | Exposição localizada, sem corrosão ativa visível | Exposição significativa, cobrimento reduzido ou corrosão ativa |
| Deformação | Inferior a 2 mm | Entre 2 mm e 5 mm | Superior a 5 mm |
| Condição estrutural | Íntegro e apto à operação | Deterioração progressiva, mas sem falha estrutural imediata | Comprometimento estrutural relevante |

### Regra de decisão

A classe final de cada imagem foi definida com base no defeito mais severo observado:

1. Se o dormente apresentava fratura, trinca severa, armadura exposta com corrosão ou deformação acentuada, a imagem foi classificada como `POOR`.
2. Se o dormente apresentava danos intermediários, como trincas moderadas, deformações leves ou exposição localizada de armadura sem corrosão ativa, a imagem foi classificada como `FAIR`.
3. Se o dormente não apresentava defeitos estruturais relevantes, a imagem foi classificada como `GOOD`.

### Observação

Como a classificação foi realizada a partir de imagens, alguns critérios dimensionais foram avaliados visualmente quando não havia medição direta disponível. Assim, a rotulagem considerou a severidade aparente dos defeitos, a extensão das trincas, a presença de armadura exposta e o estado geral do dormente.
