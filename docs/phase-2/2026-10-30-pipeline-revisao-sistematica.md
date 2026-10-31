Sim. Abaixo está um protocolo inicial pronto para adaptar ao **Parsifal**, com foco em mapear a interseção entre **cascade testing**, **Knowledge Graphs/GNNs**, **otimização** e **decisão sob restrições**. Ele foi desenhado para revelar tanto trabalhos que já ocupam o espaço quanto evidências de lacuna.

## Título provisório da revisão

**Aprendizado orientado à decisão e otimização em Knowledge Graphs familiares para priorizar rastreamento genético em cascata sob restrições clínicas, éticas e de recursos: uma revisão sistemática da literatura.**

A justificativa clínica é robusta: revisões recentes mostram adesão ao cascade testing frequentemente abaixo de 30% e fragilidade na avaliação de custo, fidelidade e sustentabilidade das intervenções.  Além disso, contato direto com familiares pode aumentar a adesão em relação ao modelo mediado pelo paciente, mas envolve questões de privacidade, infraestrutura e ética. [nature](https://www.nature.com/articles/s41525-024-00412-0)

## PICOC

| Elemento | Definição para esta revisão |
|---|---|
| **P — Population/Problem** | Famílias ou indivíduos com suspeita ou confirmação de câncer hereditário; portadores de variantes patogênicas/provavelmente patogênicas; familiares elegíveis para teste genético em cascata. |
| **I — Intervention** | Métodos de IA, aprendizado de máquina, GNNs, Knowledge Graphs, active learning, otimização matemática, pesquisa operacional, decisão sob incerteza ou sistemas de apoio à decisão usados para priorizar, planejar ou otimizar cascade testing. |
| **C — Comparison** | Prática usual, critérios clínicos tradicionais, triagem não priorizada, modelos estatísticos clássicos, heurísticas manuais ou ausência de intervenção computacional. |
| **O — Outcome** | Detecção de variantes P/LP; adesão ao teste; cobertura familiar; custo; tempo até teste; equidade; utilidade clínica; QALYs; desempenho preditivo; qualidade/explicabilidade da decisão; viabilidade operacional. |
| **C — Context** | Serviços de genética médica, oncogenética, laboratórios de diagnóstico genético, sistemas de saúde públicos ou privados; preferencialmente estudos com dados reais, mas estudos simulados e metodológicos também são elegíveis. |
| **T — Time** | 2010–2026 para estudos de cascade testing e saúde; 2015–2026 para GNNs, Knowledge Graphs e decision-focused learning, refletindo a maturidade técnica dessas áreas. |

## Perguntas de Pesquisa

**RQ1 — Estado da arte:** Quais métodos de IA, aprendizado de máquina, grafos de conhecimento ou modelos preditivos já foram aplicados ao rastreamento genético em cascata em câncer hereditário?

**RQ2 — Otimização:** Quais problemas de cascade testing já foram formalizados como problemas de otimização, alocação de recursos, planejamento sequencial, decisão sob incerteza ou otimização combinatória?

**RQ3 — Representação relacional:** Como pedigree familiar, dados genéticos, evidências clínicas e relações de parentesco têm sido representados por Knowledge Graphs, grafos familiares, ontologias ou GNNs?

**RQ4 — Integração IA + PO:** Quais abordagens integram modelos preditivos de IA com modelos de otimização — inclusive *predict-then-optimize*, *decision-focused learning*, RL ou heurísticas aprendidas — em contextos de saúde ou triagem genética?

**RQ5 — Restrições clínicas e éticas:** Quais restrições clínicas, éticas, legais, de privacidade, de equidade e de recursos são explicitamente modeladas nos estudos de priorização de cascade testing?

**RQ6 — Lacunas:** Quais lacunas persistem na integração entre GNNs/Knowledge Graphs familiares, active learning e otimização para priorizar cascade testing sob restrições reais?

A RQ4 é a mais importante para a originalidade da sua tese: *decision-focused learning* é uma área reconhecida para integrar previsão e otimização, mas sua aplicação a grafos familiares e oncogenética parece pouco explorada. 

## Perguntas secundárias

- **SQ1:** Quais variáveis de entrada são mais usadas para estimar risco ou prioridade de familiares?
- **SQ2:** Quais funções objetivo são adotadas: detecção de variantes, custo-efetividade, QALYs, cobertura, tempo, equidade ou utilidade clínica?
- **SQ3:** Quais métricas de avaliação são reportadas além de acurácia, AUC e F1?
- **SQ4:** Quais bases de dados, coortes ou simuladores são utilizados?
- **SQ5:** Há estudos que consideram incerteza nas previsões e propagam essa incerteza para a decisão?
- **SQ6:** Há relatos de implementação real, validação externa ou avaliação de impacto clínico?

## Palavras-chave e sinônimos

### Conceito 1 — Cascade testing

- “cascade testing”
- “cascade genetic testing”
- “cascade screening”
- “familial genetic testing”
- “family genetic testing”
- “predictive genetic testing”
- “genetic counseling and testing”
- “hereditary cancer syndrome”
- “hereditary cancer”
- “inherited cancer”
- “cancer predisposition”
- “germline variant”
- “pathogenic variant”
- “likely pathogenic variant”
- “pedigree”
- “family history”

### Conceito 2 — Knowledge Graph e GNN

- “knowledge graph”
- “knowledge graphs”
- “graph database”
- “ontology”
- “ontologies”
- “semantic graph”
- “family graph”
- “pedigree graph”
- “genealogical graph”
- “graph neural network”
- “graph neural networks”
- “GNN”
- “relational graph convolutional network”
- “R-GCN”
- “graph representation learning”
- “graph embedding”
- “link prediction”
- “node classification”
- “graph active learning”
- “graph sparsification”

### Conceito 3 — Otimização e decisão

- “optimization”
- “optimisation”
- “mathematical optimization”
- “mathematical programming”
- “operations research”
- “combinatorial optimization”
- “integer programming”
- “mixed integer programming”
- “MIP”
- “MILP”
- “stochastic programming”
- “robust optimization”
- “constraint optimization”
- “resource allocation”
- “resource planning”
- “scheduling”
- “sequencing”
- “prioritization”
- “prioritisation”
- “triage”
- “decision-making under uncertainty”
- “sequential decision-making”
- “Markov decision process”
- “MDP”
- “reinforcement learning”
- “decision-focused learning”
- “predict-then-optimize”
- “smart predict-then-optimize”
- “prescriptive analytics”
- “optimal experimental design”
- “active learning”
- “budgeted learning”

### Conceito 4 — Saúde, ética e restrições

- “healthcare”
- “health care”
- “clinical decision support”
- “clinical workflow”
- “genetic service”
- “genetic services”
- “genetic counseling”
- “privacy”
- “data protection”
- “GDPR”
- “LGPD”
- “ethics”
- “ethical constraints”
- “equity”
- “health equity”
- “fairness”
- “cost-effectiveness”
- “cost utility”
- “implementation”
- “sustainability”

## Strings de busca

Use estas strings como ponto de partida no Parsifal. A primeira é a **string principal**; as demais são variações para bases com sintaxes diferentes.

### String principal — Scopus, Web of Science, IEEE Xplore

```text
("cascade testing" OR "cascade genetic testing" OR "cascade screening" OR "familial genetic testing" OR "predictive genetic testing")
AND
("hereditary cancer" OR "inherited cancer" OR "cancer predisposition" OR "hereditary cancer syndrome" OR "germline variant" OR "pathogenic variant" OR "pedigree" OR "family history")
AND
("knowledge graph*" OR "graph neural network*" OR "GNN" OR "graph representation learning" OR "graph embedding" OR "ontology" OR "link prediction" OR "node classification" OR "graph active learning")
OR
("cascade testing" OR "cascade genetic testing" OR "cascade screening")
AND
("optimization" OR "optimisation" OR "operations research" OR "integer programming" OR "mixed integer programming" OR "stochastic programming" OR "resource allocation" OR "scheduling" OR "prioritization" OR "decision-making under uncertainty" OR "reinforcement learning" OR "decision-focused learning" OR "active learning")
```

### String para bases biomédicas — PubMed/MEDLINE/Embase

```text
("cascade testing"[tiab] OR "cascade genetic testing"[tiab] OR "cascade screening"[tiab] OR "familial genetic testing"[tiab] OR "predictive genetic testing"[tiab])
AND
("hereditary cancer"[tiab] OR "inherited cancer"[tiab] OR "cancer predisposition"[tiab] OR "germline variant"[tiab] OR "pathogenic variant"[tiab] OR "pedigree"[tiab] OR "family history"[tiab])
AND
("artificial intelligence"[tiab] OR "machine learning"[tiab] OR "deep learning"[tiab] OR "knowledge graph"[tiab] OR "graph neural network"[tiab] OR "optimization"[tiab] OR "operations research"[tiab] OR "resource allocation"[tiab] OR "decision support"[tiab] OR "cost-effectiveness"[tiab])
```

### String técnica — arXiv, IEEE Xplore, ACM DL

```text
("graph neural network*" OR "knowledge graph*" OR "graph representation learning" OR "relational graph convolutional network")
AND
("active learning" OR "decision-focused learning" OR "predict-then-optimize" OR "combinatorial optimization" OR "mixed integer programming" OR "stochastic optimization" OR "reinforcement learning")
AND
("healthcare" OR "health care" OR "clinical decision support" OR "genetic testing" OR "genetic counseling" OR "pedigree" OR "cascade testing" OR "resource allocation")
```

### String de checagem de lacuna — mais ampla

```text
("cascade testing" OR "cascade genetic testing" OR "cascade screening")
AND
("optimization" OR "optimisation" OR "integer programming" OR "mixed integer programming" OR "stochastic programming" OR "resource allocation" OR "scheduling" OR "prioritization" OR "decision-making under uncertainty")
```

Esta última é essencial: se ela retornar poucos resultados com formulação explícita de otimização, isso fortalece empiricamente a hipótese de lacuna do Tema B. A literatura clínica existente concentra-se em adesão, comunicação familiar, contato direto e implementação, não necessariamente em modelos prescritivos de alocação. [nature](https://www.nature.com/articles/s41525-024-00412-0)

## Critérios de elegibilidade

### Critérios de inclusão

- Artigos revisados por pares, atas de conferências relevantes, capítulos com método formal ou preprints com método e avaliação claros.
- Estudos publicados entre 2010 e 2026; para métodos de GNN, Knowledge Graphs e decision-focused learning, priorizar 2015–2026.
- Estudos sobre cascade testing, triagem genética familiar, oncogenética, doenças raras, triagem populacional ou alocação de recursos em saúde.
- Estudos que apresentem pelo menos um dos seguintes elementos: modelo preditivo, Knowledge Graph, GNN, active learning, modelo de otimização, simulação, análise de custo-efetividade ou sistema de apoio à decisão.
- Estudos em inglês, português ou espanhol.
- Estudos empíricos, metodológicos, de modelagem, revisões sistemáticas e posicionamentos conceituais relevantes — os últimos apenas para contextualização, não como evidência primária.

### Critérios de exclusão

- Estudos sem texto completo acessível.
- Artigos de opinião, editoriais, resumos de congresso sem método ou material promocional.
- Estudos que mencionem “grafo” apenas como metáfora, sem representação formal de nós, arestas ou relações.
- Estudos que mencionem “otimização” apenas como melhoria genérica, sem função objetivo, variáveis de decisão, restrições ou método de solução.
- Estudos exclusivamente sobre câncer somático, tumor sequencing ou oncologia sem componente hereditário/familiar.
- Estudos sobre cascade testing que não tragam qualquer dimensão de decisão, priorização, recurso, IA, modelagem ou avaliação quantitativa.
- Duplicatas e versões anteriores do mesmo estudo, mantendo a versão mais completa.

## Estratégia de triagem no Parsifal

### Etapa 1 — Deduplicação

Importe os resultados de todas as bases, remova duplicatas por DOI, título normalizado e similaridade título/autores/ano.

### Etapa 2 — Screening por título e resumo

Aplique os critérios de inclusão/exclusão de forma independente, idealmente por dois revisores. Para um piloto individual, use uma amostra de 50–100 registros para calibrar os critérios antes da triagem completa.

### Etapa 3 — Texto completo

Leia os artigos potencialmente elegíveis e classifique-os em:

- **Elegível — evidência primária:** propõe ou avalia método aplicável ao seu problema.
- **Elegível — contexto clínico:** caracteriza cascade testing, barreiras, adesão, custos ou políticas.
- **Elegível — método habilitador:** apresenta GNN, Knowledge Graph, active learning, otimização ou decision-focused learning aplicável.
- **Excluído — fora de escopo.**
- **Excluído — sem método/avaliação.**
- **Excluído — duplicata ou versão inferior.**

### Etapa 4 — Extração de dados

Sugiro estes campos no Parsifal:

- Título, autores, ano, veículo, DOI, tipo de estudo.
- País e contexto de saúde.
- Tipo de câncer ou síndrome hereditária.
- Tipo de dado: coorte real, registro, simulador, base pública.
- Representação do problema: tabela, pedigree, grafo, Knowledge Graph, ontologia.
- Método de IA: ML clássico, deep learning, GNN, RL, LLM, GraphRAG.
- Método de PO: MIP, MILP, programa estocástico, otimização robusta, heurística, metaheurística, simulação.
- Integração IA + PO: nenhuma, sequencial, iterativa, decision-focused, RL, heurística aprendida.
- Função objetivo.
- Variáveis de decisão.
- Restrições modeladas.
- Incerteza tratada.
- Métricas de desfecho.
- Métricas de equidade, custo e sustentabilidade.
- Validação: interna, externa, prospectiva, clínica.
- Limitações declaradas.
- Lacuna identificada.

## Critérios de qualidade

Para estudos empíricos, avalie:

- Clareza da formulação do problema.
- Qualidade dos dados e tratamento de valores ausentes.
- Baseline clínico relevante.
- Validação externa ou prospectiva.
- Avaliação além da acurácia preditiva.
- Consideração de incerteza.
- Consideração de custo, capacidade e equidade.
- Transparência ética e de privacidade.
- Reprodutibilidade: código, dados ou descrição suficiente.

Para estudos de cascade testing, use como referência os desfechos apontados pela literatura: adesão, custo, fidelidade e sustentabilidade são justamente os menos reportados, o que reforça a necessidade de incluí-los na sua extração. [nature](https://www.nature.com/articles/s41525-024-00412-0)

## Fluxograma sugerido

1. Identificação: registros recuperados nas bases.
2. Deduplicação.
3. Triagem título/resumo.
4. Triagem texto completo.
5. Inclusão final.
6. Síntese narrativa + mapa de evidências.
7. Análise de lacunas para formulação da tese.

## Resultado esperado

A revisão deve permitir classificar a literatura em quatro blocos:

1. **Clínico:** cascade testing, adesão, comunicação familiar, custo e implementação. [nature](https://www.nature.com/articles/s41525-024-00412-0)
2. **Representacional:** Knowledge Graphs, ontologias, pedigree computacional e GNNs.
3. **Decisório:** otimização, alocação de recursos, RL, active learning e decisão sob incerteza.
4. **Integrador:** trabalhos que de fato unem IA preditiva, grafos familiares e otimização prescritiva.

Se o bloco 4 for pequeno, você terá evidência forte de que sua proposta não é apenas uma aplicação a mais, mas uma **integração ainda pouco explorada** entre representação relacional, aprendizado orientado à decisão e otimização em oncogenética. [nature](https://www.nature.com/articles/s41525-024-00412-0)

Pelas telas, eu faria três ajustes principais: separar conceitos que estão agrupados como sinônimos, mover “Otimização e decisão” de *Comparison* para *Intervention* e construir a avaliação de qualidade com itens condicionais ao tipo de estudo. O formulário de extração deve registrar sobretudo a diferença entre “prever risco” e “melhorar uma decisão”.

A seguir está uma configuração **operacional** para preencher o Parsifal. Também corrijo dois pontos da orientação anterior: poucos resultados não demonstram, sozinhos, uma lacuna; e um estudo metodológico não deve receber avaliação negativa apenas por não ter validação clínica.

## 1. Keywords and Synonyms

### O que corrigir na sua configuração atual

Na imagem, “Cascade testing” agrupa procedimentos, doenças e síndromes. Esses termos estão relacionados, mas não são equivalentes:

- “Cascade genetic testing” é uma variante terminológica de “cascade testing”.
- “Hereditary cancer” descreve o contexto clínico.
- “Li-Fraumeni” é uma síndrome específica.
- “Predictive genetic testing” é mais amplo que teste em cascata.

Também recomendo separar Knowledge Graph de GNN: um é uma representação de conhecimento; o outro, uma família de modelos. Essa separação ajuda a construir buscas que encontrem trabalhos relevantes sem exigir simultaneamente todos os componentes da tese. O desenvolvimento de estratégias de busca distingue conceitos, termos livres e vocabulários controlados, com adaptação da sintaxe para cada base. [utas.libguides](https://utas.libguides.com/SystematicReviews/SearchStrategies)

### Configuração recomendada

Cada linha abaixo pode ser um registro em “Keywords and Synonyms”. A coluna de termos inclui variantes e termos relacionados para recuperação; não implica equivalência conceitual perfeita.

| Keyword | Synonyms / termos de busca | Related to |
|---|---|---|
| Hereditary cancer | hereditary cancer; inherited cancer; familial cancer; hereditary cancer syndrome; hereditary cancer predisposition; hereditary neoplasm | Population |
| Relatives and pedigrees | relative; family member; at-risk relative; biological relative; pedigree; family history; proband; index case | Population |
| Cascade genetic testing | cascade testing; cascade genetic testing; cascade screening; family cascade screening; familial variant testing | Intervention |
| Knowledge graphs | knowledge graph; biomedical knowledge graph; semantic graph; graph database; ontology; ontologies | Intervention |
| Graph neural networks | graph neural network; GNN; graph convolutional network; relational graph convolutional network; R-GCN; graph representation learning; graph embedding | Intervention |
| Mathematical optimization | mathematical optimization; mathematical optimisation; mathematical programming; operations research; operational research; integer programming; mixed-integer programming; combinatorial optimization; constraint programming | Intervention |
| Optimization under uncertainty | stochastic programming; stochastic optimization; robust optimization; distributionally robust optimization; sequential decision making; Markov decision process; partially observable Markov decision process | Intervention |
| Learning–optimization integration | decision-focused learning; decision focused learning; predict-then-optimize; predict then optimize; predict-and-optimize; smart predict-then-optimize; end-to-end optimization; prescriptive analytics | Intervention |
| Information acquisition | active learning; graph active learning; optimal experimental design; value of information; information gain; budgeted learning; cost-sensitive active learning | Intervention |
| Learned decision policies | reinforcement learning; offline reinforcement learning; policy learning; contextual bandit; learning to optimize | Intervention |
| Comparators | usual care; standard care; clinical criteria; guideline-based strategy; heuristic; rule-based strategy; risk-based prioritization; random selection; predict-then-optimize | Comparison |
| Operational outcomes | testing uptake; test completion; family coverage; carrier detection; diagnostic yield; turnaround time; resource utilization; cost-effectiveness; cost-utility; quality-adjusted life year | Outcome |
| Decision quality | decision quality; decision regret; optimality gap; feasibility; constraint violation; expected utility; net benefit | Outcome |
| Implementation context | clinical genetics; cancer genetics; genetic counseling; genetic counselling; genetics service; genetic testing service; healthcare; health care | Context |
| Ethics and equity | informed consent; confidentiality; privacy; family communication; direct relative contact; equity; fairness; access to care | Context |

“Predict-then-optimize” aparece em dois papéis possíveis: intervenção quando é o método estudado e comparador quando o estudo propõe outra integração. Essa ambiguidade deve ser resolvida na extração, não proibida no vocabulário.

### Termos que eu manteria como expansão, não como bloco obrigatório

- Síndromes e genes: Li-Fraumeni, Lynch syndrome, hereditary breast and ovarian cancer, BRCA1, BRCA2, TP53.
- Tarefas de grafo: link prediction, node classification, graph completion.
- Eficiência: graph sparsification, subgraph selection, pruning.
- Métodos específicos: MILP, POMDP, bilevel optimization, differentiable optimization.

Não exija todos esses termos na busca principal. Por exemplo, um artigo sobre otimização de testagem familiar pode não mencionar GNN, e um método relevante de *decision-focused learning* pode não mencionar genética.

### Como combinar os blocos

Proponho três trilhas, documentadas separadamente:

| Trilha | Combinação conceitual | Finalidade |
|---|---|---|
| Clínica | Cascade testing AND câncer hereditário | Identificar decisões, barreiras, custos e comparadores reais. |
| Prescritiva | Cascade testing AND otimização/decisão/alocação | Encontrar formulações diretamente aplicáveis. |
| Metodológica | Integração aprendizado–otimização AND grafos ou aquisição de informação | Identificar métodos transferíveis, mesmo fora da oncogenética. |

Na terceira trilha, a aplicabilidade ao problema precisa ser justificada na seleção. Isso está alinhado à distinção que suas notas já fazem entre relevância clínica e relevância para otimização. [pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws](https://pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws.com/projectfiles-prod/gateway-object-store/repos/files-a5f14286da803e72c73e2980894fde18/downloads/82fdb075169cc7dcfab31dad3221050e54cd9ada/README.md?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Checksum-Mode=ENABLED&X-Amz-Credential=ASIA2F3EMEYEQVE6ACLI%2F20261031%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20261031T005311Z&X-Amz-Expires=600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEHgaCXVzLWVhc3QtMSJHMEUCIQDWtwTms4ViBsgpIh0xi1Z0z7D4xA%2BiAbZSrcoIYw%2BD%2FwIgHAG8LkUu8KrqLiyhoSOU9VrAnG%2Bu5M8wNjqS9IoK2U4qpgUIQRABGgw2OTk3NTMzMDk3MDUiDNKvzHW8trjch2FhRCqDBY25D6nZ94aQVaPUIrII5nyAs80QkwnpR9ITPz7erxt0gIYI4RQijzmhUM3zfbpz6BbW8IW1Tta3HQrUQ%2Fm3SfXOgAMozHbVxFuzMuzg6b9kOuqZ6aMJsqF%2BPbTb8uV7%2BK94rFdhfRi16dUftyrQAJeT7H66MU6%2B5gDZCKHpg2h2Pnm2g75S5p4DpFmeyWfst6g%2BWin4S3lmytDErmOqrWGKscY1tYtyQOtuxcSaSMK%2FK7QkXtL7wCc5o6T3%2BeLputLuT7zcQUSkxHbNITLfR7mmowQ7p38yylcb0fxS6ETxmN3e%2BIdbDBlskgiL1CcP1dJ%2BP0UOzGO2bIEXpoFQsC8JJlPiQNh2kr%2FnX1dia%2FC9j8Q9GdqKVm2Wvdcua4%2B6w%2B%2BZMTfnBzbVwYQp%2FvIKpI2BUtBU5%2FcAK7PmkNiswLRB3GbghuGTLjvHbyvvxupmAwsw24xGowFlXtW6Q%2FWKoAh1AZ5bj%2FGh20Fg0kBHv9%2BmnfLBjmd1q3Nzv4xYHuJ%2Fu3UIsyE9LwjvJzyZk74yx5IVpRDV4qY20kpt6PVYRkrjrxFHQ5PprOwDAhb3uK5yjtULbO6NBBG3X3XKgEI81nbr6r0RzW%2FfR%2FBtbiwBEk1MF3xj1%2BDgiEMNYrIwfsyevVsu3jodIzdVCpBBv4%2BboFAVziOaZ%2BAAhF0oUGaWBcV2BheyxAaoIDN91KkpQMBS%2BMELPGksB75u6jPGc1H6DPAIucpnZnqq3AY0xQIvhSZAQ4FLh%2BQw50RdUF0c6Xf6FUAXEm01vecA3VKbLRF4uoTLzG5aaCIAE1I%2FYD2cKhphgp9clX2LV6rwajNWK1gdfKZ9kRGB%2BEtTdQ%2FvzucNITxZPP4wlt%2BU1wY6kAEGdiFxgEDM99yO6AY7O7EFg85BCZznocGD0uQwoZxTzdlic2J7X%2BNYhYTj90vlB%2BA3K5lsd70EqlEhpvD8Yoz7%2Ft34EO9Xt8f%2FsaWItqDYuYe%2B7zgJpUDpzTTYVsDij1kEPh462S1W5j9KWbTbGese%2B7xD5ZWYTdmzOQW9kt1P4BRP4wiw9y91HFzTygJpiP4%3D&X-Amz-SignedHeaders=host&response-content-type=text%2Fmarkdown%3B%20charset%3Dutf-8&x-id=GetObject&X-Amz-Signature=fd0e83a715f02e16850c36f503435cfdd87ce0f9a2fd7733c9ff3328d83955a3)

Use OR dentro dos blocos e AND entre blocos, com parênteses explícitos. Revise também descritores MeSH/Emtree quando disponíveis; a lista acima contém termos livres, não descritores controlados já validados. A diretriz PRESS recomenda revisar tradução da pergunta, operadores, descritores, termos livres, sintaxe e limites. [linkinghub.elsevier](https://linkinghub.elsevier.com/retrieve/pii/S0895435616000585)

## 2. Quality Assessment Checklist

### Primeiro: distinguir qualidade de relevância

Recomendo três classificações separadas:

1. Elegibilidade: o estudo responde a alguma pergunta da revisão?
2. Qualidade metodológica: suas conclusões são sustentadas pelo desenho e pela avaliação?
3. Transferibilidade: o método pode ser usado no seu problema?

Um artigo de otimização em outro domínio pode ter alta qualidade e transferibilidade moderada. Um estudo clínico de cascade testing pode ser diretamente relevante sem utilizar IA. Não misture essas características em um único escore.

Para modelos preditivos de saúde, o PROBAST+AI diferencia qualidade, risco de viés e aplicabilidade, organizando a avaliação em participantes/fontes de dados, preditores, desfecho e análise. O checklist abaixo é uma proposta própria para sua revisão heterogênea, não uma aplicação validada desse instrumento. [bmj](https://www.bmj.com/content/388/bmj-2024-082505)

### Questions: núcleo comum

Cadastre estas oito perguntas para todos os estudos primários:

| ID | Texto para cadastrar | Regra de avaliação |
|---|---|---|
| QA01 | O objetivo, o problema investigado e a contribuição do estudo estão claramente definidos? | Deve ser possível identificar o que o estudo pretende demonstrar. |
| QA02 | As fontes de dados ou instâncias, os critérios de seleção e a população-alvo estão suficientemente descritos? | Em simulação, avaliar geração das instâncias e hipóteses. |
| QA03 | Os métodos, pressupostos e procedimentos estão descritos com detalhe suficiente para compreensão e reprodução? | Código público ajuda, mas não é obrigatório. |
| QA04 | O desenho de avaliação é adequado às alegações do estudo? | Avaliação teórica, computacional ou clínica conforme a contribuição. |
| QA05 | Os comparadores ou referências de avaliação são apropriados e a comparação é justa? | Pode incluir solver exato, heurística, prática usual ou referência teórica. |
| QA06 | As métricas e os resultados apresentados sustentam as conclusões? | Não exigir AUC de um estudo de otimização nem impacto clínico de uma prova teórica. |
| QA07 | A incerteza ou a robustez dos resultados é avaliada de forma adequada? | Conforme aplicável: intervalos, repetições, sensibilidade, cenários ou limites teóricos. |
| QA08 | As limitações e ameaças à validade são discutidas de forma compatível com o estudo? | Inclui generalização e fragilidade de pressupostos. |

### Questions: módulos condicionais

Cadastre também os itens seguintes, usando “Não aplicável” quando o componente não existir.

| ID | Pergunta | Aplicar quando |
|---|---|---|
| QA09 | O estudo previne vazamento de informação e justifica a separação entre desenvolvimento e avaliação? | Modelos aprendidos a partir de dados. |
| QA10 | O tratamento de dados ausentes, desbalanceamento e seleção de variáveis é descrito e adequado? | Modelos preditivos empíricos. |
| QA11 | A avaliação preditiva contempla aspectos relevantes ao uso pretendido, incluindo calibração quando probabilidades orientam decisões? | Predição utilizada para decisão ou risco individual. |
| QA12 | As variáveis de decisão, a função objetivo e as restrições são explicitamente definidas? | Otimização prescritiva. |
| QA13 | A avaliação da solução considera viabilidade e qualidade de solução, além do valor da função objetivo? | Otimização prescritiva. |
| QA14 | O estudo avalia o efeito das previsões sobre as decisões, em vez de reportar somente desempenho preditivo? | Integração IA–PO. |
| QA15 | A representação do grafo e o protocolo de avaliação evitam o uso de relações ou informações indisponíveis no momento da decisão? | Estudos com grafos. |
| QA16 | O uso de dados e as intervenções envolvendo pessoas têm justificativa ética e procedimentos de consentimento ou dispensa adequadamente reportados? | Dados humanos ou intervenção com participantes. |

Em QA09 e QA15, registre especificamente se pacientes da mesma família aparecem em treino e teste e se isso é compatível com o cenário de uso. Compartilhamento familiar não é automaticamente um erro: a pergunta é se a avaliação estima generalização para novas famílias, novos familiares de famílias conhecidas ou outro cenário. Vazamento de dados pode produzir estimativas excessivamente otimistas de desempenho. [bmj](https://www.bmj.com/content/388/bmj-2024-082505)

### Answers e Weight

Configuração sugerida:

| Description | Weight |
|---|---:|
| Sim — atende adequadamente | 1 |
| Parcialmente — atende com limitações | 0,5 |
| Não — não atende ou não apresenta evidência suficiente | 0 |
| Não aplicável — justificar | 0 |

O peso zero de “Não aplicável” é apenas uma solução de cadastro. Ele não deve ser interpretado como falha.

No escore analítico, exclua itens não aplicáveis do denominador:

\[
Q=\frac{\sum_{j\in A}s_j}{|A|}\times100,
\]

em que \(A\) é o conjunto de perguntas aplicáveis e \(s_j\) vale 0, 0,5 ou 1.

### Max Score e Cutoff Score

Com 16 perguntas e peso máximo 1, o máximo nominal será 16. Contudo, estudos com menos itens aplicáveis não podem ser comparados pelo total bruto.

Minha proposta para esta revisão exploratória:

- Cutoff Score: 0, para não excluir automaticamente por soma.
- Usar o escore normalizado e o perfil por item na síntese.
- Registrar falhas críticas separadamente: vazamento relevante, ausência de avaliação compatível com a conclusão ou decisões inviáveis não reconhecidas.
- Não considerar o checklist customizado um substituto de instrumentos específicos de risco de viés.

Se o Parsifal não descontar “Não aplicável”, calcule o percentual normalizado na planilha de síntese. Não use o escore bruto exibido como ranking de qualidade.

## 3. Data Extraction Form

Sugiro um formulário com núcleo obrigatório e módulos condicionais. Abaixo, “Texto” significa o tipo textual disponível na sua versão; “Select one” e “Select many” correspondem às opções mencionadas na tela.

Nos campos condicionais, inclua as opções “Não aplicável” e “Não reportado”. Elas representam situações diferentes.

### A. Identificação e papel na revisão

| Description | Type | Values / instrução |
|---|---|---|
| Study ID | Texto | Identificador único, ligando artigos do mesmo estudo. |
| Referência e DOI | Texto | Evitar repetir se o cadastro bibliográfico já for suficiente. |
| Tipo de estudo | Select many | Observacional; experimental; desenvolvimento de modelo; avaliação de modelo; otimização computacional; teórico; simulação; avaliação econômica; implementação. |
| Papel na revisão | Select many | Evidência clínica direta; método integrador direto; método transferível; contexto. |
| Perguntas de pesquisa respondidas | Select many | RQ1; RQ2; RQ3; RQ4; RQ5; RQ6. |
| Status de publicação | Select one | Revisado por pares; preprint; outro. |
| Objetivo e contribuição principal | Texto | Resumir sem reproduzir a conclusão dos autores como fato confirmado. |

Revisões sistemáticas podem formar um corpus secundário para contexto e snowballing. Evite contar uma revisão e seus estudos incluídos como evidências primárias independentes.

### B. Contexto clínico e dados

| Description | Type | Values / instrução |
|---|---|---|
| Domínio e contexto assistencial | Texto | Oncogenética, laboratório, aconselhamento, sistema público/privado etc. |
| Síndrome, gene ou condição | Texto | BRCA1/2, TP53, Lynch etc. |
| Origem dos dados | Select many | Institucional; multicêntrica; registro; base pública; sintética; benchmark. |
| Tamanho e unidades de análise | Texto | Separar pessoas, famílias, probandos, variantes, nós, arestas e instâncias. |
| População elegível e seleção | Texto | Como os participantes ou instâncias entraram no estudo. |
| Informação disponível na decisão | Texto | Dados conhecidos antes de escolher a ação. |
| Dados ausentes e viés de seleção | Texto | Procedimentos e limitações reportados. |

### C. Representação relacional e IA

| Description | Type | Values / instrução |
|---|---|---|
| Representação dos dados | Select many | Tabular; pedigree; grafo homogêneo; grafo heterogêneo; Knowledge Graph; temporal; outra. |
| Schema do grafo | Texto | Nós, arestas, atributos, direção e temporalidade. |
| Método de IA | Select many | Nenhum; estatístico; ML clássico; GNN; RL; outro. |
| Tarefa de aprendizado | Select many | Classificação; regressão; link prediction; aquisição de informação; aprendizado de política; outra. |
| Alvo predito | Texto | Portador, adesão, custo, risco, vínculo familiar etc. |
| Protocolo de validação | Select many | Interna; temporal; geográfica; externa; prospectiva; avaliação simulada. |
| Unidade de particionamento e prevenção de vazamento | Texto | Indivíduo, família, instituição, tempo; relações disponíveis em treino/teste. |
| Métricas preditivas e calibração | Texto | Valor, conjunto avaliado e incerteza, quando reportados. |

### D. Problema de decisão e Pesquisa Operacional

| Description | Type | Values / instrução |
|---|---|---|
| Decisão apoiada | Texto | Quem testar, convidar, coletar informação ou priorizar. |
| Variáveis de decisão | Texto | O que o algoritmo escolhe efetivamente. |
| Função objetivo | Texto | Expressão ou descrição, unidades e horizonte temporal. |
| Restrições | Select many | Orçamento; capacidade; elegibilidade; precedência; tempo; consentimento; privacidade; equidade; outra. |
| Formalização das restrições | Texto | Distinguir restrição matemática de discussão narrativa. |
| Método de PO | Select many | Programação inteira; estocástica; robusta; programação dinâmica; programação por restrições; heurística; metaheurística; outro. |
| Incerteza e atualização | Texto | Parâmetros incertos, distribuições, cenários e atualização após resultados. |
| Método de solução e esforço computacional | Texto | Solver, versão, hardware, tempo limite e configurações. |
| Garantias e qualidade de solução | Texto | Prova, aproximação, gap, limites ou ausência de garantia. |

### E. Integração IA–PO e resultados

| Description | Type | Values / instrução |
|---|---|---|
| Arquitetura principal da integração | Select one | Sem integração; predict-then-optimize; decision-focused learning; IA auxilia solver; otimização auxilia aprendizado; política aprendida; híbrida; outra. |
| Fluxo de informação IA–PO | Texto | O que é predito, como entra na decisão e qual perda orienta o treinamento. |
| Comparadores | Texto | Prática clínica, heurística, modelo simples, solver, política etc. |
| Desfechos decisórios e operacionais | Texto | Regret, utilidade, custo, cobertura, adesão, viabilidade e tempo. |
| Desfechos clínicos | Texto | Distinguir desfecho observado de benefício projetado em modelo. |
| Avaliação econômica | Texto | Perspectiva, horizonte, moeda/ano, custos e desfechos. |
| Equidade, ética e supervisão humana | Texto | Medida, mecanismo, restrição ou discussão apenas. |
| Resultado principal e incerteza | Texto | Resultado quantitativo e comparador correspondente. |
| Limitações declaradas pelos autores | Texto | Registrar separadamente da sua crítica. |
| Limitações identificadas pelo revisor | Texto | Julgamento fundamentado. |
| Transferibilidade e dados necessários | Texto | O que seria necessário para aplicar ao seu cenário. |
| Evidência para possível lacuna | Texto | Componente ausente e limites da inferência. |
| Localização da evidência | Texto | Página, seção, tabela ou figura. |

O campo “Fluxo de informação IA–PO” é central: distingue uma contribuição em melhoria do aprendizado de uma aplicação que usa previsões prontas para otimizar a operação. Essa distinção preserva seu objetivo de pesquisar otimização aplicada à IA, registrado nas notas do projeto. [pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws](https://pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws.com/projectfiles-prod/gateway-object-store/repos/files-a5f14286da803e72c73e2980894fde18/downloads/82fdb075169cc7dcfab31dad3221050e54cd9ada/README.md?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Checksum-Mode=ENABLED&X-Amz-Credential=ASIA2F3EMEYEQVE6ACLI%2F20261031%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20261031T005311Z&X-Amz-Expires=600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEHgaCXVzLWVhc3QtMSJHMEUCIQDWtwTms4ViBsgpIh0xi1Z0z7D4xA%2BiAbZSrcoIYw%2BD%2FwIgHAG8LkUu8KrqLiyhoSOU9VrAnG%2Bu5M8wNjqS9IoK2U4qpgUIQRABGgw2OTk3NTMzMDk3MDUiDNKvzHW8trjch2FhRCqDBY25D6nZ94aQVaPUIrII5nyAs80QkwnpR9ITPz7erxt0gIYI4RQijzmhUM3zfbpz6BbW8IW1Tta3HQrUQ%2Fm3SfXOgAMozHbVxFuzMuzg6b9kOuqZ6aMJsqF%2BPbTb8uV7%2BK94rFdhfRi16dUftyrQAJeT7H66MU6%2B5gDZCKHpg2h2Pnm2g75S5p4DpFmeyWfst6g%2BWin4S3lmytDErmOqrWGKscY1tYtyQOtuxcSaSMK%2FK7QkXtL7wCc5o6T3%2BeLputLuT7zcQUSkxHbNITLfR7mmowQ7p38yylcb0fxS6ETxmN3e%2BIdbDBlskgiL1CcP1dJ%2BP0UOzGO2bIEXpoFQsC8JJlPiQNh2kr%2FnX1dia%2FC9j8Q9GdqKVm2Wvdcua4%2B6w%2B%2BZMTfnBzbVwYQp%2FvIKpI2BUtBU5%2FcAK7PmkNiswLRB3GbghuGTLjvHbyvvxupmAwsw24xGowFlXtW6Q%2FWKoAh1AZ5bj%2FGh20Fg0kBHv9%2BmnfLBjmd1q3Nzv4xYHuJ%2Fu3UIsyE9LwjvJzyZk74yx5IVpRDV4qY20kpt6PVYRkrjrxFHQ5PprOwDAhb3uK5yjtULbO6NBBG3X3XKgEI81nbr6r0RzW%2FfR%2FBtbiwBEk1MF3xj1%2BDgiEMNYrIwfsyevVsu3jodIzdVCpBBv4%2BboFAVziOaZ%2BAAhF0oUGaWBcV2BheyxAaoIDN91KkpQMBS%2BMELPGksB75u6jPGc1H6DPAIucpnZnqq3AY0xQIvhSZAQ4FLh%2BQw50RdUF0c6Xf6FUAXEm01vecA3VKbLRF4uoTLzG5aaCIAE1I%2FYD2cKhphgp9clX2LV6rwajNWK1gdfKZ9kRGB%2BEtTdQ%2FvzucNITxZPP4wlt%2BU1wY6kAEGdiFxgEDM99yO6AY7O7EFg85BCZznocGD0uQwoZxTzdlic2J7X%2BNYhYTj90vlB%2BA3K5lsd70EqlEhpvD8Yoz7%2Ft34EO9Xt8f%2FsaWItqDYuYe%2B7zgJpUDpzTTYVsDij1kEPh462S1W5j9KWbTbGese%2B7xD5ZWYTdmzOQW9kt1P4BRP4wiw9y91HFzTygJpiP4%3D&X-Amz-SignedHeaders=host&response-content-type=text%2Fmarkdown%3B%20charset%3Dutf-8&x-id=GetObject&X-Amz-Signature=fd0e83a715f02e16850c36f503435cfdd87ce0f9a2fd7733c9ff3328d83955a3)

## 4. Regras de preenchimento para evitar conclusões enviesadas

Inclua no protocolo estas regras:

> “Não reportado” não significa “não realizado”. “Não aplicável” não constitui deficiência metodológica. Ausência de avaliação clínica não invalida contribuição metodológica, mas limita alegações de benefício assistencial.

> Restrições éticas serão classificadas conforme sua implementação: discussão narrativa, critério de elegibilidade, procedimento operacional, restrição matemática ou avaliação empírica.

> Desfechos simulados ou projetados serão diferenciados de desfechos observados em pacientes e serviços.

> A ausência de estudos recuperados será interpretada considerando cobertura das bases, estratégia de busca, limites e busca por referências; não será tomada isoladamente como prova de originalidade.

Essa cautela também aparece nas suas notas: o Tema B permanece uma oportunidade a validar, e a ausência de formulações de otimização em uma rodada não foi tratada como demonstração definitiva de lacuna. [pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws](https://pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws.com/projectfiles-prod/gateway-object-store/repos/files-a5f14286da803e72c73e2980894fde18/downloads/82fdb075169cc7dcfab31dad3221050e54cd9ada/themes.md?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Checksum-Mode=ENABLED&X-Amz-Credential=ASIA2F3EMEYEQVE6ACLI%2F20261031%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20261031T005311Z&X-Amz-Expires=600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEHgaCXVzLWVhc3QtMSJHMEUCIQDWtwTms4ViBsgpIh0xi1Z0z7D4xA%2BiAbZSrcoIYw%2BD%2FwIgHAG8LkUu8KrqLiyhoSOU9VrAnG%2Bu5M8wNjqS9IoK2U4qpgUIQRABGgw2OTk3NTMzMDk3MDUiDNKvzHW8trjch2FhRCqDBY25D6nZ94aQVaPUIrII5nyAs80QkwnpR9ITPz7erxt0gIYI4RQijzmhUM3zfbpz6BbW8IW1Tta3HQrUQ%2Fm3SfXOgAMozHbVxFuzMuzg6b9kOuqZ6aMJsqF%2BPbTb8uV7%2BK94rFdhfRi16dUftyrQAJeT7H66MU6%2B5gDZCKHpg2h2Pnm2g75S5p4DpFmeyWfst6g%2BWin4S3lmytDErmOqrWGKscY1tYtyQOtuxcSaSMK%2FK7QkXtL7wCc5o6T3%2BeLputLuT7zcQUSkxHbNITLfR7mmowQ7p38yylcb0fxS6ETxmN3e%2BIdbDBlskgiL1CcP1dJ%2BP0UOzGO2bIEXpoFQsC8JJlPiQNh2kr%2FnX1dia%2FC9j8Q9GdqKVm2Wvdcua4%2B6w%2B%2BZMTfnBzbVwYQp%2FvIKpI2BUtBU5%2FcAK7PmkNiswLRB3GbghuGTLjvHbyvvxupmAwsw24xGowFlXtW6Q%2FWKoAh1AZ5bj%2FGh20Fg0kBHv9%2BmnfLBjmd1q3Nzv4xYHuJ%2Fu3UIsyE9LwjvJzyZk74yx5IVpRDV4qY20kpt6PVYRkrjrxFHQ5PprOwDAhb3uK5yjtULbO6NBBG3X3XKgEI81nbr6r0RzW%2FfR%2FBtbiwBEk1MF3xj1%2BDgiEMNYrIwfsyevVsu3jodIzdVCpBBv4%2BboFAVziOaZ%2BAAhF0oUGaWBcV2BheyxAaoIDN91KkpQMBS%2BMELPGksB75u6jPGc1H6DPAIucpnZnqq3AY0xQIvhSZAQ4FLh%2BQw50RdUF0c6Xf6FUAXEm01vecA3VKbLRF4uoTLzG5aaCIAE1I%2FYD2cKhphgp9clX2LV6rwajNWK1gdfKZ9kRGB%2BEtTdQ%2FvzucNITxZPP4wlt%2BU1wY6kAEGdiFxgEDM99yO6AY7O7EFg85BCZznocGD0uQwoZxTzdlic2J7X%2BNYhYTj90vlB%2BA3K5lsd70EqlEhpvD8Yoz7%2Ft34EO9Xt8f%2FsaWItqDYuYe%2B7zgJpUDpzTTYVsDij1kEPh462S1W5j9KWbTbGese%2B7xD5ZWYTdmzOQW9kt1P4BRP4wiw9y91HFzTygJpiP4%3D&X-Amz-SignedHeaders=host&response-content-type=text%2Fmarkdown%3B%20charset%3Dutf-8&x-id=GetObject&X-Amz-Signature=ecb089d8a3d505b32ef54ace85ba40141f3d31ee1f7128b467396344415b0550)

## 5. Ordem prática de implementação

1. Reorganize “Keywords and Synonyms” conforme os blocos acima.
2. Cadastre as 16 perguntas de qualidade e as quatro respostas.
3. Mantenha o corte em zero durante o piloto.
4. Cadastre os campos de extração por módulos.
5. Faça um piloto proposto de seis estudos: dois clínicos, dois de PO e dois de integração IA–PO.
6. Ajuste ambiguidades, congele a versão do protocolo e registre alterações posteriores.

O resultado será um formulário capaz de responder não apenas “quem já juntou essas tecnologias?”, mas “qual decisão foi formalizada, quais dados sustentam essa decisão e que evidência demonstra melhoria?”. Essa é a unidade de comparação mais útil para definir sua contribuição de doutorado.