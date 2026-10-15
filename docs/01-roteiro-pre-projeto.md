Sim — dá para transformar os três eixos em um pré-projeto coeso para o ICMC: **um framework de otimização multiobjetivo que seleciona/poda subgrafos de uma base de conhecimento, respeitando restrições ontológicas e escolhendo ativamente quais partes rotular/treinar**. Seu material do OncoGeneGraph fornece um caso de aplicação forte em oncogenética, com grafo de pacientes, famílias, variantes, genes e evidências. [pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws](https://pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws.com/projectfiles-prod/gateway-object-store/repos/files-a5f14286da803e72c73e2980894fde18/downloads/2b4ca6634f0c665a5c98b3e9bc5c66958f75762e/pesquisa-phd.md?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Checksum-Mode=ENABLED&X-Amz-Credential=ASIA2F3EMEYEZLON66CL%2F20261015%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20261015T150359Z&X-Amz-Expires=600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEAMaCXVzLWVhc3QtMSJHMEUCIAZ6v0wfW%2FWa6ixYZlW3FM2LMajGl0WATe8Sve%2FY1r6fAiEAjvSL1vT63m%2BpmJVVYJStQo4ezq%2B62m8XCl9P%2Bcg25x0qsAUIy%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARABGgw2OTk3NTMzMDk3MDUiDMMkrDTMVbWgQxRSIiqEBU2nSV7rM4PudsxFfcmwWQH4INvYgEozXaZ5dUYbcI7F6sHdHPd24EVglaNnq8yXw%2FPUPZF6DkyJ5sQFfhlrzQOLef48aXtF4tx1xwDkEXK9O8%2FoUnH1oHl4yL21So8lplV%2BsWYHrgsKF20Rghqyozhq3CzTH5re3cOLptAvLsLE1M0YoW%2B3m1WWAei78WODtMIFzDdOt3m%2Fk17yF88P7FGohha0xF%2FKqSI14BlhLpL23kM9h0Vhsd0gZJOu8eK0fY2VQQ586wy4R%2FoA3nbzPr96Tq4cHszsdEIRpmzWx2WJMJUo13HQl7RkU8gjbilQYqJHrvCXLCnaddrmAPjLQI6JDS6Bwb5LuP07HoVsNphwyUThCfM5qgohe%2F3%2FsyLPDJVHcWsxPO8i59JVqgeWX9jWJ%2FFUIyL1WfuCwvA8r7ThtvCjDw6z7DgixIntpOD7wc63n1E7N5Jg%2BtwD4N4q72oSBP11DIu1sv4r7kBNTI83qk9U5EG0v5CwWtTIruBEal0IH1uBqpay4k7ZXsA2%2BFlCm9QSsNnvN%2BYkkn3WHLWB8pgI3c31yh0fpSjxxvjNrH8TzraUY%2F7t5oGiO5cvelQbITGaDtwZy0XKoQVUthVAU0b4zkB%2FjDmDaFCAb8Z6zsNJWCzCG0i3V35om390HKbCLKLl1JuxbIVb0S84DJfZDSYXldWHU9zVWJTOkylTY8tFhhWJ8A9dIjxYiLr%2FT3Etd%2FTlN5izCSeQgnH3IPbXjiVj4t10TLqXn5kU3PISfmUGh%2BjoAGAPtfpjDFN827SKBBRH2GXnny%2FqmTQUU%2BIeZpsXC6tyMJwLXXIoPrTdLd1HtJKepFH0lezK0H2Z8NIqonv1MP%2FOwtYGOpAB3nIVUAWg6FYfn%2BZPE6U8ZN9k1TOzwEEIHjzRViZgDvZiWYYr4ARXbNcYfptbj3k9TIJIblyrJLUy%2FoW%2BnCmnNiWX82CRn2gRf97KDZ8otFwRw5k7Jo64APxDIyDH7A0Kk9aw9r9zClj63KjH%2Fn%2FjXiDSii6HqJe8ONQ9PIMxj3PTzhrX2f1YZSmqGuMIPdqW&X-Amz-SignedHeaders=host&x-id=GetObject&X-Amz-Signature=beb4efd40657520da7f635a6fab022750d1ab9fcc7d63ead8ae093eb9f835ee3)

## Título sugerido

**Otimização multiobjetivo consciente de ontologia para poda e aprendizado ativo de subgrafos em redes neurais de grafos**

Alternativa mais aplicada:

**Poda ontologicamente consciente e aprendizado ativo de subgrafos por otimização multiobjetivo para GNNs em grafos de conhecimento biomédicos**

## Problema de pesquisa

GNNs sobre grafos de conhecimento grandes e heterogêneos enfrentam três tensões simultâneas:

- **Escala computacional:** processar o grafo completo ou um número excessivo de subgrafos é caro; métodos recentes de seleção de subgrafos buscam reduzir esse custo mantendo desempenho.[3]
- **Qualidade semântica:** remover nós, arestas ou relações pode destruir caminhos relevantes, quebrar hierarquias e produzir subgrafos estatisticamente bons, mas semanticamente inválidos ou injustos.
- **Escassez de rótulos:** em saúde, anotação especializada é cara; aprendizado ativo em grafos busca selecionar os nós mais informativos para rotulação. [arxiv](https://arxiv.org/html/2310.20082v2)

A lacuna é que poda, seleção de subgrafos e aprendizado ativo costumam ser tratados separadamente, sem um mecanismo único que equilibre **desempenho preditivo, custo computacional, validade ontológica, cobertura da estrutura e custo de anotação**.

## Hipótese central

É possível formular a construção de subgrafos para treino e inferência de GNNs como um problema de **otimização multiobjetivo restrita**, em que a poda é guiada pela ontologia do domínio e o aprendizado ativo direciona a coleta de rótulos para regiões do grafo de maior valor informacional.

Formalmente, dado um grafo de conhecimento \(G=(V,E,R)\), uma ontologia \(O\) e um orçamento de anotação \(B\), buscar um subgrafo \(S \subseteq G\) que aproxime a fronteira de Pareto entre:

\[
\max f_{\text{desempenho}}(S),\quad
\min f_{\text{custo}}(S),\quad
\max f_{\text{cobertura}}(S),\quad
\max f_{\text{validade}}(S),\quad
\min f_{\text{incerteza}}(S)
\]

sujeito a restrições ontológicas, como preservação de tipos, hierarquias, relações obrigatórias, consistência lógica e trilhas de evidência relevantes.

## Objetivo geral

Desenvolver e avaliar um framework de **poda consciente de ontologia** para GNNs, no qual a seleção de subgrafos e a priorização de anotações sejam resolvidas como um problema multiobjetivo, com avaliação em grafos de conhecimento biomédicos.

## Objetivos específicos

1. **Formalizar poda ontologicamente consciente:** definir quais elementos podem ser removidos, quais devem ser preservados e como as restrições da ontologia entram no problema de otimização.
2. **Modelar o problema multiobjetivo:** construir funções-objetivo e restrições para acurácia/AUC, sparsidade, tempo de inferência, cobertura de entidades/relações, validade semântica e incerteza preditiva.
3. **Desenvolver algoritmos de seleção de subgrafos:** comparar formulações baseadas em programação inteira/mista, heurísticas evolutivas, aprendizado por reforço e políticas diferenciáveis de seleção.
4. **Integrar aprendizado ativo:** usar incerteza, diversidade estrutural, representatividade de tipos e valor esperado de redução de erro para escolher nós/arestas a rotular dentro do orçamento.
5. **Avaliar em cenário real:** aplicar o framework a um grafo genético-laboratorial e familiar de câncer hereditário, com tarefas de classificação de risco e predição de vínculos familiares. [pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws](https://pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws.com/projectfiles-prod/gateway-object-store/repos/files-a5f14286da803e72c73e2980894fde18/downloads/2b4ca6634f0c665a5c98b3e9bc5c66958f75762e/pesquisa-phd.md?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Checksum-Mode=ENABLED&X-Amz-Credential=ASIA2F3EMEYEZLON66CL%2F20261015%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20261015T150359Z&X-Amz-Expires=600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEAMaCXVzLWVhc3QtMSJHMEUCIAZ6v0wfW%2FWa6ixYZlW3FM2LMajGl0WATe8Sve%2FY1r6fAiEAjvSL1vT63m%2BpmJVVYJStQo4ezq%2B62m8XCl9P%2Bcg25x0qsAUIy%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARABGgw2OTk3NTMzMDk3MDUiDMMkrDTMVbWgQxRSIiqEBU2nSV7rM4PudsxFfcmwWQH4INvYgEozXaZ5dUYbcI7F6sHdHPd24EVglaNnq8yXw%2FPUPZF6DkyJ5sQFfhlrzQOLef48aXtF4tx1xwDkEXK9O8%2FoUnH1oHl4yL21So8lplV%2BsWYHrgsKF20Rghqyozhq3CzTH5re3cOLptAvLsLE1M0YoW%2B3m1WWAei78WODtMIFzDdOt3m%2Fk17yF88P7FGohha0xF%2FKqSI14BlhLpL23kM9h0Vhsd0gZJOu8eK0fY2VQQ586wy4R%2FoA3nbzPr96Tq4cHszsdEIRpmzWx2WJMJUo13HQl7RkU8gjbilQYqJHrvCXLCnaddrmAPjLQI6JDS6Bwb5LuP07HoVsNphwyUThCfM5qgohe%2F3%2FsyLPDJVHcWsxPO8i59JVqgeWX9jWJ%2FFUIyL1WfuCwvA8r7ThtvCjDw6z7DgixIntpOD7wc63n1E7N5Jg%2BtwD4N4q72oSBP11DIu1sv4r7kBNTI83qk9U5EG0v5CwWtTIruBEal0IH1uBqpay4k7ZXsA2%2BFlCm9QSsNnvN%2BYkkn3WHLWB8pgI3c31yh0fpSjxxvjNrH8TzraUY%2F7t5oGiO5cvelQbITGaDtwZy0XKoQVUthVAU0b4zkB%2FjDmDaFCAb8Z6zsNJWCzCG0i3V35om390HKbCLKLl1JuxbIVb0S84DJfZDSYXldWHU9zVWJTOkylTY8tFhhWJ8A9dIjxYiLr%2FT3Etd%2FTlN5izCSeQgnH3IPbXjiVj4t10TLqXn5kU3PISfmUGh%2BjoAGAPtfpjDFN827SKBBRH2GXnny%2FqmTQUU%2BIeZpsXC6tyMJwLXXIoPrTdLd1HtJKepFH0lezK0H2Z8NIqonv1MP%2FOwtYGOpAB3nIVUAWg6FYfn%2BZPE6U8ZN9k1TOzwEEIHjzRViZgDvZiWYYr4ARXbNcYfptbj3k9TIJIblyrJLUy%2FoW%2BnCmnNiWX82CRn2gRf97KDZ8otFwRw5k7Jo64APxDIyDH7A0Kk9aw9r9zClj63KjH%2Fn%2FjXiDSii6HqJe8ONQ9PIMxj3PTzhrX2f1YZSmqGuMIPdqW&X-Amz-SignedHeaders=host&x-id=GetObject&X-Amz-Signature=beb4efd40657520da7f635a6fab022750d1ab9fcc7d63ead8ae093eb9f835ee3)
6. **Avaliar explicabilidade e segurança:** medir se os subgrafos selecionados preservam evidências interpretáveis e evitam remoção de caminhos clinicamente relevantes.

## Estrutura do pré-projeto

### 1. Introdução

Apresente que GNNs são adequadas para dados relacionais, mas sua aplicação em grafos de conhecimento reais exige lidar com escala, heterogeneidade, escassez de rótulos e restrições semânticas. A literatura recente reconhece escalabilidade, dinamicidade e heterogeneidade como desafios centrais de GNNs. [mlgworkshop](http://www.mlgworkshop.org/2023/papers/MLG__KDD_2023_paper_9.pdf)

Delimite a contribuição: não propor apenas “mais uma GNN”, mas um **método de otimização para decidir o que o modelo deve ver, o que pode ser descartado e o que merece ser anotado**.

### 2. Fundamentação teórica

| Eixo | Conteúdo mínimo | Papel no projeto |
|---|---|---|
| Grafos de conhecimento e ontologias | Tipos de entidades, relações, hierarquias, axiomas, consistência | Define restrições e penalidades da poda |
| GNNs relacionais | R-GCN, GAT, GraphSAGE, message passing | Modelo preditivo sobre o subgrafo |
| Poda e seleção de subgrafos | Poda de arestas/nós, amostragem de vizinhança, seleção aprendida de subgrafos | Reduz custo e ruído sem perder informação relevante  [ieeexplore.ieee](https://ieeexplore.ieee.org/iel8/6287639/11323511/11397632.pdf) |
| Otimização multiobjetivo | Pareto, scalarização, restrições, algoritmos evolutivos, otimização diferenciável | Equilibra objetivos conflitantes |
| Aprendizado ativo em grafos | Incerteza, diversidade, representatividade, seleção sequencial | Otimiza o uso de rótulos caros  [arxiv](https://arxiv.org/html/2310.20082v2) |

Uma referência útil para a parte de otimização é a taxonomia e revisão de *multi-objective deep learning*, que organiza métodos conforme paradigma de aprendizado e necessidades do decisor. [link.springer](https://link.springer.com/article/10.1007/s44443-025-00105-3)

### 3. Formulação do problema

Proponha a seguinte decomposição:

- **Variável de decisão:** máscara binária ou contínua sobre nós, arestas e relações; opcionalmente, variáveis de seleção de amostras para anotação.
- **Objetivo 1 — desempenho:** maximizar métrica da tarefa, como AUC-ROC, AUC-PR, F1 ou acurácia.
- **Objetivo 2 — eficiência:** minimizar número de nós/arestas, memória, FLOPs ou tempo de inferência.
- **Objetivo 3 — fidelidade semântica:** maximizar aderência à ontologia, por exemplo preservação de caminhos tipo–relação–tipo e de relações obrigatórias.
- **Objetivo 4 — cobertura:** evitar que a poda elimine subpopulações, famílias, genes ou categorias de variantes relevantes.
- **Objetivo 5 — custo de anotação:** minimizar quantidade de novos rótulos solicitados.
- **Restrições duras:** integridade referencial, tipos válidos, relações obrigatórias, privacidade e limites éticos.

Isso permite unir os três temas: a **ontologia** define o espaço viável; a **otimização multiobjetivo** escolhe o subgrafo; o **aprendizado ativo** realimenta o processo com rótulos seletivos.

### 4. Metodologia proposta

**Fase 1 — Representação do grafo e ontologia**

- Construir um grafo heterogêneo com pacientes, familiares, variantes, genes, fenótipos, exames, classificações e evidências externas.
- Definir um schema/ontologia mínima: tipos, hierarquias, cardinalidades e regras de consistência.
- Criar subgrafos de referência, por exemplo TP53, BRCA1/2 e Lynch, como no planejamento do OncoGeneGraph. [pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws](https://pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws.com/projectfiles-prod/gateway-object-store/repos/files-a5f14286da803e72c73e2980894fde18/downloads/2b4ca6634f0c665a5c98b3e9bc5c66958f75762e/pesquisa-phd.md?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Checksum-Mode=ENABLED&X-Amz-Credential=ASIA2F3EMEYEZLON66CL%2F20261015%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20261015T150359Z&X-Amz-Expires=600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEAMaCXVzLWVhc3QtMSJHMEUCIAZ6v0wfW%2FWa6ixYZlW3FM2LMajGl0WATe8Sve%2FY1r6fAiEAjvSL1vT63m%2BpmJVVYJStQo4ezq%2B62m8XCl9P%2Bcg25x0qsAUIy%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARABGgw2OTk3NTMzMDk3MDUiDMMkrDTMVbWgQxRSIiqEBU2nSV7rM4PudsxFfcmwWQH4INvYgEozXaZ5dUYbcI7F6sHdHPd24EVglaNnq8yXw%2FPUPZF6DkyJ5sQFfhlrzQOLef48aXtF4tx1xwDkEXK9O8%2FoUnH1oHl4yL21So8lplV%2BsWYHrgsKF20Rghqyozhq3CzTH5re3cOLptAvLsLE1M0YoW%2B3m1WWAei78WODtMIFzDdOt3m%2Fk17yF88P7FGohha0xF%2FKqSI14BlhLpL23kM9h0Vhsd0gZJOu8eK0fY2VQQ586wy4R%2FoA3nbzPr96Tq4cHszsdEIRpmzWx2WJMJUo13HQl7RkU8gjbilQYqJHrvCXLCnaddrmAPjLQI6JDS6Bwb5LuP07HoVsNphwyUThCfM5qgohe%2F3%2FsyLPDJVHcWsxPO8i59JVqgeWX9jWJ%2FFUIyL1WfuCwvA8r7ThtvCjDw6z7DgixIntpOD7wc63n1E7N5Jg%2BtwD4N4q72oSBP11DIu1sv4r7kBNTI83qk9U5EG0v5CwWtTIruBEal0IH1uBqpay4k7ZXsA2%2BFlCm9QSsNnvN%2BYkkn3WHLWB8pgI3c31yh0fpSjxxvjNrH8TzraUY%2F7t5oGiO5cvelQbITGaDtwZy0XKoQVUthVAU0b4zkB%2FjDmDaFCAb8Z6zsNJWCzCG0i3V35om390HKbCLKLl1JuxbIVb0S84DJfZDSYXldWHU9zVWJTOkylTY8tFhhWJ8A9dIjxYiLr%2FT3Etd%2FTlN5izCSeQgnH3IPbXjiVj4t10TLqXn5kU3PISfmUGh%2BjoAGAPtfpjDFN827SKBBRH2GXnny%2FqmTQUU%2BIeZpsXC6tyMJwLXXIoPrTdLd1HtJKepFH0lezK0H2Z8NIqonv1MP%2FOwtYGOpAB3nIVUAWg6FYfn%2BZPE6U8ZN9k1TOzwEEIHjzRViZgDvZiWYYr4ARXbNcYfptbj3k9TIJIblyrJLUy%2FoW%2BnCmnNiWX82CRn2gRf97KDZ8otFwRw5k7Jo64APxDIyDH7A0Kk9aw9r9zClj63KjH%2Fn%2FjXiDSii6HqJe8ONQ9PIMxj3PTzhrX2f1YZSmqGuMIPdqW&X-Amz-SignedHeaders=host&x-id=GetObject&X-Amz-Signature=beb4efd40657520da7f635a6fab022750d1ab9fcc7d63ead8ae093eb9f835ee3)

**Fase 2 — Poda consciente de ontologia**

- Implementar pontuações de importância estrutural, semântica e preditiva.
- Remover apenas elementos cuja exclusão não viole regras ontológicas nem degrade caminhos de evidência.
- Comparar poda estática, poda baseada em gradiente/atenção e poda guiada por restrições ontológicas.

**Fase 3 — Otimização multiobjetivo**

- Comparar pelo menos três estratégias:
  - soma ponderada / scalarização;
  - restrições epsilon;
  - algoritmos evolutivos multiobjetivo, como NSGA-II;
  - política aprendida de seleção de subgrafos.
- Gerar frente de Pareto entre precisão, tamanho do subgrafo, validade semântica e custo.

**Fase 4 — Aprendizado ativo de subgrafos**

- Selecionar nós ou arestas para anotação com base em incerteza do modelo, diversidade estrutural e representatividade ontológica.
- Usar ciclos: treinar GNN → identificar subgrafo de alta incerteza/valor → solicitar rótulo especializado → atualizar grafo e política de poda.
- O trabalho sobre aprendizado ativo em grafos formula a escolha de nós como processo sequencial e usa uma política aprendida para reduzir custo de anotação. [arxiv](https://arxiv.org/html/2310.20082v2)

**Fase 5 — Avaliação**

- **Baselines:** GNN no grafo completo; amostragem aleatória de subgrafos; poda por grau/PageRank; poda sem restrição ontológica; aprendizado ativo por incerteza simples.
- **Métricas:** AUC-ROC, AUC-PR, F1, calibração, sparsidade, tempo de treino/inferência, cobertura, violações ontológicas, número de rótulos necessários e estabilidade entre execuções.
- **Análise de Pareto:** hipervolume, espalhamento e dominância entre soluções.
- **Explicabilidade:** verificar se as evidências retidas continuam rastreáveis e clinicamente interpretáveis.

## Cronograma sugerido — 48 meses

| Período | Atividade | Entrega |
|---|---|---|
| M1–M6 | Revisão sistemática; definição do problema; levantamento de dados e ontologia | Protocolo de revisão; schema preliminar |
| M7–M12 | Construção do grafo; baseline GNN; definição formal do problema | Artigo de posicionamento ou workshop; código-base |
| M13–M18 | Poda consciente de ontologia | Método e experimentos preliminares |
| M19–M24 | Formulação multiobjetivo e algoritmos de seleção | Artigo principal de método |
| M25–M30 | Integração com aprendizado ativo | Framework completo |
| M31–M36 | Avaliação extensiva, ablações e análise de Pareto | Artigo de avaliação |
| M37–M42 | Estudo de caso em oncogenética; explicabilidade e robustez | Estudo aplicado |
| M43–M48 | Tese, reprodutibilidade e disseminação | Tese e repositório |

## Contribuições esperadas

- Uma **formalização** de poda de grafos de conhecimento como problema multiobjetivo restrito pela ontologia.
- Um **algoritmo ou família de algoritmos** que selecione subgrafos adaptativos, em vez de usar amostragem aleatória ou heurísticas fixas.
- Uma **estratégia de aprendizado ativo** que priorize anotações de maior valor considerando estrutura, semântica e incerteza.
- Uma **avaliação empírica** em domínio de alto impacto, com grafos biomédicos e tarefas de classificação/predição de vínculos.
- Um **repositório open-source** com benchmarks, schema ontológico, métricas e pipelines reproduzíveis.

## Fontes iniciais

- **Efficient Subgraph GNNs by Learning Effective Selection Policies** — aprende políticas de seleção de subgrafos para reduzir o custo computacional de Subgraph GNNs; base direta para o eixo de poda/seleção.[3]
- **Dynamic subgraph pruning and causal-aware knowledge distillation** — propõe poda dinâmica de subgrafos temporais, preservando dependências relevantes; útil para discutir poda que mantém estrutura essencial. [ieeexplore.ieee](https://ieeexplore.ieee.org/iel8/6287639/11323511/11397632.pdf)
- **Knowledge Graph Pruning for Recommendation** — aborda poda de knowledge graph com pontuações de importância e destilação de sinais colaborativos; útil como referência de poda orientada a importância. [sciencedirect](https://www.sciencedirect.com/science/article/pii/S2666827025000830)
- **Graph Policy Network for Transferable Active Learning on Graphs** — formula aprendizado ativo em grafos como decisão sequencial e aprende uma política de seleção de nós. [arxiv](https://arxiv.org/html/2310.20082v2)
- **Active Learning for Graphs with Noisy Structures** — discute seleção de nós valiosos para rotulação quando a estrutura do grafo contém ruído. [proceedings.neurips](https://proceedings.neurips.cc/paper/2020/hash/73740ea85c4ec25f00f9acbd859f861d-Abstract.html)
- **Improving Graph Neural Networks by combining active learning with self-training** — propõe o framework STAL, combinando aprendizado ativo e auto-treinamento em dados gráficos não rotulados. [dl.acm](https://dl.acm.org/doi/10.1145/3769107)
- **Multi-objective Deep Learning: Taxonomy and Survey of the State of the Art** — revisão e taxonomia de otimização multiobjetivo em deep learning; base para justificar a formulação Pareto. [link.springer](https://link.springer.com/article/10.1007/s44443-025-00105-3)
- **A Survey on Graph Neural Networks** — panorama de GNNs e desafios de escalabilidade e heterogeneidade. [mlgworkshop](http://www.mlgworkshop.org/2023/papers/MLG__KDD_2023_paper_9.pdf)

## Como conectar ao seu contexto

Seu projeto anterior já prevê um knowledge graph genético-laboratorial e familiar, com R-GCN para classificação de risco e predição de vínculos familiares ausentes.  Isso é um excelente testbed porque a poda não pode ser apenas estatística: remover uma relação familiar, uma variante rara ou uma evidência clínica pode alterar radicalmente a interpretação. [pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws](https://pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws.com/projectfiles-prod/gateway-object-store/repos/files-a5f14286da803e72c73e2980894fde18/downloads/2b4ca6634f0c665a5c98b3e9bc5c66958f75762e/pesquisa-phd.md?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Checksum-Mode=ENABLED&X-Amz-Credential=ASIA2F3EMEYEZLON66CL%2F20261015%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20261015T150359Z&X-Amz-Expires=600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEAMaCXVzLWVhc3QtMSJHMEUCIAZ6v0wfW%2FWa6ixYZlW3FM2LMajGl0WATe8Sve%2FY1r6fAiEAjvSL1vT63m%2BpmJVVYJStQo4ezq%2B62m8XCl9P%2Bcg25x0qsAUIy%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARABGgw2OTk3NTMzMDk3MDUiDMMkrDTMVbWgQxRSIiqEBU2nSV7rM4PudsxFfcmwWQH4INvYgEozXaZ5dUYbcI7F6sHdHPd24EVglaNnq8yXw%2FPUPZF6DkyJ5sQFfhlrzQOLef48aXtF4tx1xwDkEXK9O8%2FoUnH1oHl4yL21So8lplV%2BsWYHrgsKF20Rghqyozhq3CzTH5re3cOLptAvLsLE1M0YoW%2B3m1WWAei78WODtMIFzDdOt3m%2Fk17yF88P7FGohha0xF%2FKqSI14BlhLpL23kM9h0Vhsd0gZJOu8eK0fY2VQQ586wy4R%2FoA3nbzPr96Tq4cHszsdEIRpmzWx2WJMJUo13HQl7RkU8gjbilQYqJHrvCXLCnaddrmAPjLQI6JDS6Bwb5LuP07HoVsNphwyUThCfM5qgohe%2F3%2FsyLPDJVHcWsxPO8i59JVqgeWX9jWJ%2FFUIyL1WfuCwvA8r7ThtvCjDw6z7DgixIntpOD7wc63n1E7N5Jg%2BtwD4N4q72oSBP11DIu1sv4r7kBNTI83qk9U5EG0v5CwWtTIruBEal0IH1uBqpay4k7ZXsA2%2BFlCm9QSsNnvN%2BYkkn3WHLWB8pgI3c31yh0fpSjxxvjNrH8TzraUY%2F7t5oGiO5cvelQbITGaDtwZy0XKoQVUthVAU0b4zkB%2FjDmDaFCAb8Z6zsNJWCzCG0i3V35om390HKbCLKLl1JuxbIVb0S84DJfZDSYXldWHU9zVWJTOkylTY8tFhhWJ8A9dIjxYiLr%2FT3Etd%2FTlN5izCSeQgnH3IPbXjiVj4t10TLqXn5kU3PISfmUGh%2BjoAGAPtfpjDFN827SKBBRH2GXnny%2FqmTQUU%2BIeZpsXC6tyMJwLXXIoPrTdLd1HtJKepFH0lezK0H2Z8NIqonv1MP%2FOwtYGOpAB3nIVUAWg6FYfn%2BZPE6U8ZN9k1TOzwEEIHjzRViZgDvZiWYYr4ARXbNcYfptbj3k9TIJIblyrJLUy%2FoW%2BnCmnNiWX82CRn2gRf97KDZ8otFwRw5k7Jo64APxDIyDH7A0Kk9aw9r9zClj63KjH%2Fn%2FjXiDSii6HqJe8ONQ9PIMxj3PTzhrX2f1YZSmqGuMIPdqW&X-Amz-SignedHeaders=host&x-id=GetObject&X-Amz-Signature=beb4efd40657520da7f635a6fab022750d1ab9fcc7d63ead8ae093eb9f835ee3)