# Protocolo consolidado de revisão da literatura

## 1. Título provisório

Aprendizado orientado à decisão e otimização em Knowledge Graphs familiares para priorizar rastreamento genético em cascata sob restrições clínicas, éticas e de recursos: um mapeamento sistemático da literatura.

## 2. Finalidade e delimitação

Este protocolo propõe um **mapeamento** sistemático da literatura, com avaliação crítica dos estudos, para identificar como Inteligência Artificial e Pesquisa Operacional podem ser integradas no planejamento do rastreamento genético em cascata em câncer hereditário.

A revisão investigará métodos para representar relações familiares e evidências genéticas, estimar probabilidades relevantes e apoiar decisões sobre priorização de testes, aquisição de informações e alocação de recursos. Também examinará métodos transferíveis de outros domínios, desde que sua relação com o problema seja explicitamente justificada.

O objetivo não é confirmar antecipadamente a originalidade da proposta, mas identificar evidências favoráveis, resultados negativos, abordagens concorrentes e limitações que permitam formular uma contribuição de doutorado tecnicamente consistente e clinicamente relevante. Nas notas atuais do projeto, a otimização do cascade testing permanece uma hipótese de oportunidade: a ausência de formulações em uma rodada exploratória não demonstra ausência na literatura. [pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws](https://pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws.com/projectfiles-prod/gateway-object-store/repos/files-a5f14286da803e72c73e2980894fde18/downloads/82fdb075169cc7dcfab31dad3221050e54cd9ada/snowballing.md?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Checksum-Mode=ENABLED&X-Amz-Credential=ASIA2F3EMEYETJE6MIIR%2F20261027%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20261027T024723Z&X-Amz-Expires=600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEBoaCXVzLWVhc3QtMSJIMEYCIQDsk4IeJRCDwvzcwpPsbWP8w%2BsNgXgUlo1ONwja9svbyAIhAIlecvLv0NhSUekGgG1kjYGZN41q6LEWcoy0ajTfO3TIKrAFCOL%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQARoMNjk5NzUzMzA5NzA1IgyVANeu7JlDnVMmGDMqhAVI4zp19Ya7FFYhno%2FllT4paoER4OTQp5nC0CeU8Lr5J%2FJ6uUf%2FWdOy99wlRZo2xTIdxH%2FpT88zK2VT7RvlwTg4F0Z%2BvRW4eB3mqH0owVTNyxRBxGgok%2FABDujy0PODCkRa3cPIhOcuWDGRPMWohqtxLvL9sovLmpW7SOPBmJO9xlPF8AW6z5UWvAoZBCgcJEIKYnrtSst0PIBPyG2%2F1b%2BhN%2BNMbFChOOOUalnj8ixxCJ6WisTo3uXRPRUDi4e%2F7MesOLP8sqZa4glm5tMonz%2B3zFOPlx67t3qs487Ne5517NXsJlwBnr1UYCOm3MM2RlFZpL9CXdGtuKMX4dtkBA1wbbShnNflxs7Y7MB5zXNJ9bEBG6Sw9bX5Ccuf0xIv%2BKnKRlDzkUQLY0KHCW7p7bHeBsYwqxjIwJgnYcAa5NPPhyX%2FVAR1xF4sYmPmaEy4Wxgn2NJYg2wcEiPYTTgltfdFUSaY%2F5SpjNYzEKRr%2FHiXdwxYEyX05hO8FbQptsFB6nUK65uJ1%2F67OJOBwxV2PNmviVYUG7w3hpQP7Ci9pqtysknLHQwMIVCkxoFexSSuLhRrCRx%2BaW0mkfvq95X7Q3UQFGHExxHBx9xYKQ5l%2F6fRMmJIZ0Xt3gms5rL%2B6jG0Fvxhc%2FIVhDDTary3belo11Qrl2X2UsqAipmtlKUpFXPiZkiL04%2FGoMnEtqFWEcvg3QeHkk9CfyD%2BB35uB%2ByX8vLuRbLFA%2Bq3bX8avK9gxQdbL9G4978k6rurJI5Om%2FWSJpBa4lz2G1vB7zGUjCNO6KSIcMQ6cg32dgFztpxFpgalwNcr7T4M75g9vPy0FywIqttzGZyw7NHGOvhC2WLvC%2Fzu361eGjDRjIDXBjqPAXhhRahFwnWtDwg5r1%2FmHTw2x6clSyf5A6%2FoyQv2GkSjWjyJCoxJvP1cf%2B%2B4NlcglVxBspUCZUpn9q7zOxbyx0tLe7fRRTnshkPAdU1CoIxYLVtKTnqdWd6%2FcZTsYv21Xz%2BGRDNkC%2BjcoWwjchKv2uFRzp3qaGf3J18L6mOGQjcPQUGpd0LCROKelwdHlvCw&X-Amz-SignedHeaders=host&response-content-type=text%2Fmarkdown%3B%20charset%3Dutf-8&x-id=GetObject&X-Amz-Signature=a4e12dfc00bb20e1f8c703541b783c7f6bb7dc25c32225e13c6a35b20dd22383)

Serão distinguidos dois tipos de contribuição:

1. Otimização da operação assistencial: usar previsões para decidir quem priorizar, quando agir e como alocar recursos.
2. Melhoria dos métodos de IA: desenvolver aprendizado orientado à decisão, aquisição ótima de informação, representações relacionais ou algoritmos que melhorem o aprendizado e sua integração com a decisão.

Essa distinção permitirá verificar se a futura tese contribui apenas com uma aplicação ou também com avanços metodológicos em IA e otimização.

## 3. Objetivos

### Objetivo geral

Mapear e avaliar criticamente métodos de IA, representação relacional e otimização aplicáveis à priorização do rastreamento genético em cascata, identificando como tratam incerteza, custos, capacidade operacional, restrições clínicas, ética e equidade.

### Objetivos específicos

- Caracterizar os problemas decisórios e operacionais do cascade testing em câncer hereditário.
- Identificar representações computacionais de pedigrees, relações familiares e evidências genéticas.
- Mapear formulações de otimização para seleção, sequenciamento e aquisição de informação.
- Identificar integrações entre aprendizado e otimização, incluindo predict-then-optimize, decision-focused learning e heurísticas aprendidas.
- Examinar desfechos preditivos, decisórios, operacionais, econômicos e clínicos.
- Avaliar qualidade metodológica, risco de viés e transferibilidade.
- Identificar lacunas sustentadas pelo corpus, sem equiparar baixa recuperação bibliográfica a originalidade.

## 4. PICOC

| Elemento | Definição |
|---|---|
| Population/Problem | Pessoas e famílias com suspeita ou confirmação de predisposição hereditária ao câncer, incluindo probandos e familiares elegíveis para investigação genética; problemas de priorização associados a informações incompletas e recursos limitados. |
| Intervention | Métodos de IA, Knowledge Graphs, GNNs, aquisição ativa de informação e otimização usados para representar, prever, priorizar ou planejar o rastreamento familiar. |
| Comparison | Prática usual, estratégias baseadas em diretrizes, probabilidades mendelianas, modelos estatísticos, heurísticas, seleção aleatória, políticas simples ou arquiteturas alternativas de integração IA–PO. |
| Outcome | Qualidade da decisão, identificação de portadores, adesão, cobertura familiar, custo, tempo, viabilidade, equidade, utilidade clínica, desempenho preditivo e eficiência computacional. |
| Context | Oncogenética, aconselhamento genético, laboratórios e serviços de saúde; adicionalmente, contextos metodológicos transferíveis com grafos, informação incompleta e decisões sob restrições. |

A ausência de comparador não excluirá automaticamente estudos teóricos ou descritivos relevantes. Sua adequação será avaliada em relação à contribuição alegada.

O período de publicação será definido separadamente do PICOC. Propõe-se inicialmente não impor limite inferior, evitando excluir métodos clássicos de pedigree e otimização; a atualização dos métodos será examinada na síntese por ano de publicação.

## 5. Perguntas de pesquisa

| ID | Pergunta |
|---|---|
| RQ1 | Quais decisões, barreiras e necessidades operacionais caracterizam o rastreamento genético em cascata em câncer hereditário? |
| RQ2 | Como pedigrees, relações familiares e evidências genéticas e clínicas são representados computacionalmente? |
| RQ3 | Quais problemas de priorização, seleção, sequenciamento e aquisição de informação foram formalizados como problemas de otimização? |
| RQ4 | Como métodos de aprendizado são integrados à otimização e qual componente do sistema é efetivamente melhorado? |
| RQ5 | Como incerteza, restrições clínicas, recursos, ética, privacidade e equidade são incorporados e avaliados? |
| RQ6 | Quais evidências sustentam a eficácia, robustez, transferibilidade e viabilidade dessas abordagens, e quais lacunas permanecem? |

A extração também investigará dados utilizados, funções objetivo, variáveis de decisão, comparadores, protocolos de validação, garantias algorítmicas e disponibilidade de recursos para reprodução.

## 6. Organização do corpus

A literatura será organizada em três conjuntos complementares:

| Conjunto | Escopo | Papel na revisão |
|---|---|---|
| Clínico | Cascade testing em câncer hereditário, comunicação familiar, adesão, implementação, custos e acesso. | Definir o problema e seus desfechos relevantes. |
| Integrador direto | Modelos computacionais, preditivos ou prescritivos aplicados à testagem genética familiar. | Identificar soluções diretamente concorrentes ou complementares. |
| Metodológico transferível | Integração IA–PO, decisão em grafos e aquisição de informação sob restrições, mesmo fora da oncogenética. | Identificar métodos aplicáveis e possíveis contribuições de base. |

Revisões anteriores serão utilizadas como corpus secundário para contextualização e busca por referências. Seus estudos primários serão avaliados individualmente, evitando dupla contagem de evidências.

## 7. Keywords and Synonyms

Os termos serão cadastrados por conceito. Termos relacionados poderão compartilhar um bloco de recuperação, mas não serão tratados como equivalentes conceituais.

| Conceito | Termos livres iniciais | PICOC |
|---|---|---|
| Câncer hereditário | hereditary cancer; inherited cancer; familial cancer; hereditary cancer syndrome; hereditary cancer predisposition; hereditary neoplasm | Population |
| Familiares e pedigrees | relative; family member; at-risk relative; biological relative; pedigree; family history; proband; index case | Population |
| Testagem em cascata | cascade testing; cascade genetic testing; cascade screening; family cascade screening; familial variant testing | Intervention |
| Representação de conhecimento | knowledge graph; biomedical knowledge graph; semantic graph; graph database; ontology; ontologies | Intervention |
| Aprendizado em grafos | graph neural network; GNN; graph convolutional network; relational graph convolutional network; R-GCN; graph representation learning; graph embedding | Intervention |
| Otimização matemática | mathematical optimization; mathematical optimisation; mathematical programming; operations research; operational research; integer programming; mixed-integer programming; combinatorial optimization; constraint programming | Intervention |
| Decisão sob incerteza | stochastic programming; stochastic optimization; robust optimization; distributionally robust optimization; sequential decision making; Markov decision process; partially observable Markov decision process | Intervention |
| Integração IA–PO | decision-focused learning; decision focused learning; predict-then-optimize; predict-and-optimize; smart predict-then-optimize; end-to-end optimization; prescriptive analytics | Intervention |
| Aquisição de informação | active learning; graph active learning; optimal experimental design; value of information; information gain; budgeted learning; cost-sensitive active learning | Intervention |
| Políticas aprendidas | reinforcement learning; offline reinforcement learning; policy learning; contextual bandit; learning to optimize | Intervention |
| Comparadores | usual care; standard care; guideline-based strategy; clinical criteria; heuristic; rule-based strategy; random selection | Comparison |
| Resultados | testing uptake; test completion; carrier detection; diagnostic yield; family coverage; cost-effectiveness; cost-utility; decision regret; optimality gap; feasibility; expected utility | Outcome |
| Contexto e implementação | clinical genetics; cancer genetics; genetic counseling; genetic counselling; genetics service; healthcare; health care | Context |
| Ética e equidade | informed consent; confidentiality; privacy; family communication; direct relative contact; equity; fairness; access to care | Context |

Li-Fraumeni, Lynch syndrome, hereditary breast and ovarian cancer, BRCA1, BRCA2 e TP53 serão usados em buscas complementares. Tarefas como link prediction, graph completion, subgraph selection e graph sparsification também poderão ampliar a trilha metodológica.

Não será obrigatório recuperar simultaneamente câncer hereditário, Knowledge Graph, GNN, otimização e ética. Essa exigência poderia eliminar estudos relevantes que tratam apenas parte da integração.

## 8. Fontes de informação

As buscas principais serão distribuídas entre fontes biomédicas e computacionais:

- PubMed/MEDLINE;
- Embase, se disponível;
- Scopus;
- Web of Science;
- IEEE Xplore;
- ACM Digital Library.

ScienceDirect e SpringerLink serão utilizados como fontes complementares e para obtenção de textos. arXiv será pesquisado separadamente para métodos recentes, mantendo identificação explícita de preprints.

Google Scholar, OpenAlex e Semantic Scholar poderão apoiar descoberta e rastreamento de citações. Para cada fonte serão registrados data da consulta, estratégia completa, campos pesquisados, filtros e quantidade de registros recuperados.

## 9. Estratégias de busca

As strings abaixo são estratégias conceituais iniciais. Antes da execução definitiva, serão adaptadas aos campos, operadores, truncamentos e vocabulários controlados de cada base. A revisão da estratégia considerará os componentes recomendados pela diretriz PRESS: tradução da pergunta, operadores, descritores, termos livres, sintaxe e limites. [linkinghub.elsevier](https://linkinghub.elsevier.com/retrieve/pii/S0895435616000585)

### Trilha 1 — Contexto clínico

```text
(
  "cascade testing"
  OR "cascade genetic testing"
  OR "cascade screening"
  OR "familial variant testing"
)
AND
(
  "hereditary cancer"
  OR "inherited cancer"
  OR "familial cancer"
  OR "hereditary cancer syndrome"
  OR "cancer predisposition"
  OR "Lynch syndrome"
  OR "Li-Fraumeni"
  OR "hereditary breast and ovarian cancer"
)
```

Essa trilha não exigirá IA nem otimização, permitindo recuperar evidências sobre o problema clínico e operacional.

### Trilha 2 — Modelagem e decisão diretamente relacionadas à testagem familiar

```text
(
  "cascade testing"
  OR "cascade genetic testing"
  OR "cascade screening"
  OR "familial variant testing"
)
AND
(
  optimization OR optimisation
  OR "operations research"
  OR "operational research"
  OR "mathematical programming"
  OR "integer programming"
  OR "resource allocation"
  OR prioritization OR prioritisation
  OR "decision analysis"
  OR "decision support"
  OR "sequential decision"
  OR "value of information"
  OR "machine learning"
  OR "artificial intelligence"
  OR "knowledge graph"
  OR "graph neural network"
)
```

A restrição a câncer hereditário será avaliada no piloto e, quando necessário, aplicada na triagem para preservar a sensibilidade.

### Trilha 3 — Métodos transferíveis

```text
(
  "decision-focused learning"
  OR "decision focused learning"
  OR "predict-then-optimize"
  OR "predict-and-optimize"
  OR "smart predict-then-optimize"
  OR "learning to optimize"
  OR "prescriptive analytics"
)
AND
(
  graph OR graphs
  OR pedigree
  OR "resource allocation"
  OR screening
  OR "active learning"
  OR "information acquisition"
  OR "optimal experimental design"
)
```

### Trilha 4 — Aquisição de informação em grafos sob restrições

```text
(
  "graph neural network"
  OR "knowledge graph"
  OR pedigree
  OR "graph active learning"
)
AND
(
  "active learning"
  OR "value of information"
  OR "optimal experimental design"
  OR "information acquisition"
)
AND
(
  budget OR budgeted
  OR cost OR "cost-sensitive"
  OR optimization OR optimisation
  OR constraint OR constraints
)
```

As estratégias serão calibradas com estudos-semente reconhecidamente relevantes. A recuperação desses estudos verificará problemas da busca, mas não será considerada prova de completude.

## 10. Critérios de seleção

### Inclusão

Serão incluídos estudos que:

1. Respondam a pelo menos uma pergunta de pesquisa.
2. Apresentem evidência clínica pertinente ao cascade testing ou método computacional diretamente aplicável ou justificadamente transferível.
3. Descrevam método, análise teórica ou avaliação de forma suficiente para exame crítico.
4. Sejam artigos completos de periódicos, conferências, capítulos metodológicos ou preprints identificáveis.
5. Estejam em inglês, português ou espanhol.
6. Utilizem dados reais, sintéticos, benchmarks ou formulações teóricas compatíveis com a contribuição proposta.

Nos estudos metodológicos externos ao domínio clínico, a inclusão exigirá justificativa registrada de transferibilidade: estrutura de grafo, aquisição de informação, incerteza ou restrições equivalentes às do problema-alvo.

### Exclusão

Serão excluídos:

- Trabalhos fora dos conjuntos clínico, integrador ou metodológico definidos.
- Resumos sem informação suficiente, materiais promocionais e opiniões sem contribuição utilizável para as perguntas da revisão.
- Trabalhos que usem “otimização” apenas como melhoria genérica, quando selecionados para o corpus de otimização formal.
- Estudos de câncer exclusivamente somático sem conexão com o problema familiar ou contribuição metodológica transferível.
- Versões redundantes sem resultados adicionais relevantes.

Estudos clínicos de comunicação, adesão e implementação não serão excluídos por não utilizarem IA. Da mesma forma, estudos metodológicos não serão excluídos por não apresentarem validação clínica.

Textos não obtidos após tentativas documentadas serão classificados como “não recuperados”, distinguindo indisponibilidade de inelegibilidade científica.

## 11. Condução e registro no Parsifal

O processo seguirá esta sequência:

1. Cadastrar objetivos, PICOC, perguntas, fontes, strings e critérios.
2. Executar buscas piloto e revisar a recuperação e o volume.
3. Consolidar a versão inicial do protocolo.
4. Importar resultados e remover duplicatas.
5. Realizar triagem por título e resumo.
6. Avaliar textos completos e registrar motivos de exclusão.
7. Aplicar avaliação de qualidade.
8. Extrair e sintetizar dados.
9. Realizar busca por referências e citações.
10. Atualizar as buscas antes do encerramento da revisão.

A deduplicação considerará DOI, título, autores e ano. Publicações diferentes do mesmo estudo receberão um identificador comum. Quando preprint e artigo final coexistirem, será utilizada preferencialmente a versão mais completa, preservando resultados exclusivos pertinentes.

Propõe-se um piloto de seis estudos para calibrar avaliação e extração: dois clínicos, dois de otimização e dois de integração IA–PO. Idealmente, a seleção será realizada por dois revisores; caso haja apenas um revisor principal, a limitação e qualquer verificação independente serão explicitadas.

Alterações posteriores ao protocolo serão registradas com data, motivo e efeito sobre a seleção.

## 12. Quality Assessment Checklist

A avaliação separará elegibilidade, qualidade metodológica e transferibilidade. O checklist será próprio da revisão e não será apresentado como instrumento validado de risco de viés. Para modelos preditivos de saúde, poderá ser complementado pelo PROBAST+AI, que diferencia qualidade, risco de viés e aplicabilidade. [bmj](https://www.bmj.com/content/388/bmj-2024-082505)

### Perguntas comuns

| ID | Pergunta |
|---|---|
| QA01 | O objetivo, o problema investigado e a contribuição estão claramente definidos? |
| QA02 | As fontes de dados ou instâncias, os critérios de seleção e a população-alvo estão suficientemente descritos? |
| QA03 | Métodos, pressupostos e procedimentos estão descritos com detalhe suficiente para compreensão e reprodução? |
| QA04 | O desenho de avaliação é adequado às alegações do estudo? |
| QA05 | Os comparadores ou referências de avaliação são apropriados e a comparação é justa? |
| QA06 | As métricas e os resultados sustentam as conclusões? |
| QA07 | A incerteza ou a robustez dos resultados é avaliada adequadamente? |
| QA08 | As limitações e ameaças à validade são discutidas de forma compatível com o estudo? |

### Perguntas condicionais

| ID | Pergunta | Aplicação |
|---|---|---|
| QA09 | O estudo previne vazamento de informação e justifica a separação entre desenvolvimento e avaliação? | Modelos aprendidos. |
| QA10 | O tratamento de dados ausentes, desbalanceamento e seleção de variáveis é descrito e adequado? | Modelos preditivos empíricos. |
| QA11 | A avaliação preditiva contempla aspectos relevantes ao uso, incluindo calibração quando probabilidades orientam decisões? | Predição de risco ou apoio à decisão. |
| QA12 | Variáveis de decisão, função objetivo e restrições são explicitamente definidas? | Otimização prescritiva. |
| QA13 | A avaliação considera viabilidade e qualidade da solução, além do valor da função objetivo? | Otimização prescritiva. |
| QA14 | O estudo avalia o efeito das previsões sobre as decisões, em vez de somente o desempenho preditivo? | Integração IA–PO. |
| QA15 | A representação do grafo e a avaliação evitam informações indisponíveis no momento da decisão? | Estudos com grafos. |
| QA16 | O uso de dados e intervenções com pessoas apresenta justificativa ética e procedimentos de consentimento ou dispensa adequadamente reportados? | Dados humanos ou intervenções. |

No caso de famílias, será registrado se a avaliação pretende generalizar para novas famílias ou para novos familiares de famílias conhecidas. A adequação do particionamento será julgada segundo esse cenário, e não apenas pela presença de parentes em conjuntos diferentes.

### Respostas e pontuação

| Resposta | Peso |
|---|---:|
| Sim — atende adequadamente | 1 |
| Parcialmente — atende com limitações | 0,5 |
| Não — não atende ou não apresenta evidência suficiente | 0 |
| Não aplicável — justificar | 0 no cadastro; excluído do denominador analítico |

O escore normalizado será:

\[
Q=\frac{\sum_{j\in A}s_j}{|A|}\times100,
\]

em que \(A\) representa os itens aplicáveis.

O cutoff inicial no Parsifal será zero, evitando exclusão automática por soma. O escore bruto não será usado para comparar estudos com diferentes números de itens aplicáveis. Se necessário, o cálculo normalizado será realizado na planilha de síntese.

Falhas críticas serão registradas separadamente. Uma média elevada não compensará, por exemplo, vazamento relevante ou avaliação incompatível com a conclusão.

## 13. Data Extraction Form

O formulário será organizado em módulos. Campos condicionais distinguirão “Não aplicável” de “Não reportado”.

| Módulo | Campos |
|---|---|
| Identificação | Study ID; referência; DOI; ano; veículo; status de publicação; vínculo entre versões. |
| Papel na revisão | Tipo de estudo; conjunto do corpus; perguntas respondidas; objetivo; contribuição principal. |
| Contexto clínico | País; serviço; população; síndrome; gene; critérios de elegibilidade; processo assistencial. |
| Dados | Origem; período; tamanho; pessoas; famílias; probandos; variantes; instâncias; dados ausentes; viés de seleção. |
| Representação relacional | Tipo de grafo; nós; arestas; atributos; direção; temporalidade; ontologia; fontes de conhecimento. |
| IA | Método; tarefa; alvo predito; entradas; treinamento; seleção de hiperparâmetros; calibração; explicabilidade. |
| Validação | Particionamento; unidade de separação; prevenção de vazamento; validação interna, externa, temporal ou prospectiva. |
| Decisão | Ação apoiada; decisor; informação disponível; horizonte; decisão única ou sequencial; atualização após resultados. |
| PO | Variáveis; função objetivo; restrições; incerteza; formulação; solver; algoritmo; parâmetros; esforço computacional. |
| Integração IA–PO | Arquitetura; fluxo de informação; perda de treinamento; papel das previsões; componente efetivamente melhorado. |
| Comparadores | Prática usual; probabilidades mendelianas; modelos simples; heurísticas; solver; políticas alternativas. |
| Resultados | Métricas preditivas, decisórias, operacionais, econômicas, clínicas e computacionais; estimativas de incerteza. |
| Ética e equidade | Consentimento; privacidade; supervisão; acesso; critérios de equidade; forma de implementação. |
| Reprodutibilidade | Código; dados; instâncias; configurações; materiais suplementares. |
| Análise crítica | Limitações dos autores; limitações do revisor; transferibilidade; dados necessários; possível lacuna. |
| Rastreabilidade | Página, seção, tabela ou figura que sustenta cada achado relevante. |

A arquitetura IA–PO será classificada como:

- Sem integração.
- Predict-then-optimize.
- Decision-focused learning.
- IA auxiliando o solver.
- Otimização auxiliando o aprendizado.
- Política aprendida.
- Arquitetura híbrida ou outra.

A classificação será acompanhada de descrição textual. O uso do rótulo pelos autores não substituirá a inspeção do fluxo de informação e do treinamento.

## 14. Regras de interpretação

A extração e a síntese seguirão estas regras:

- “Não reportado” não será interpretado automaticamente como “não realizado”.
- “Não aplicável” não constituirá deficiência metodológica.
- Ausência de validação clínica limitará alegações assistenciais, mas não invalidará automaticamente uma contribuição teórica ou computacional.
- Desfechos observados serão separados de benefícios simulados ou projetados.
- Estimativa de risco, priorização de teste e recomendação de contato serão tratadas como decisões distintas.
- Uma GNN não será presumida superior a modelos mendelianos, estatísticos ou tabulares.
- Restrições éticas serão classificadas como discussão narrativa, critério de elegibilidade, procedimento operacional, restrição matemática ou avaliação empírica.
- Resultados negativos e ausência de vantagem sobre baselines serão preservados na síntese.

## 15. Busca complementar por referências e citações

Será realizado snowballing retrospectivo, examinando referências, e prospectivo, examinando trabalhos citantes.

Os artigos-semente existentes serão usados como ponto de partida, mas não serão automaticamente considerados elegíveis. A mesma regra valerá para candidatos já registrados nas notas.

Para o snowballing, será mantida a regra proposta no projeto: encerrar após duas rodadas consecutivas sem novos estudos prioritários elegíveis. Essa regra se aplica à busca por citações, não substitui a execução das buscas nas bases. O registro atual indica que a condição ainda não havia sido atingida. [pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws](https://pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws.com/projectfiles-prod/gateway-object-store/repos/files-a5f14286da803e72c73e2980894fde18/downloads/82fdb075169cc7dcfab31dad3221050e54cd9ada/snowballing.md?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Checksum-Mode=ENABLED&X-Amz-Credential=ASIA2F3EMEYETJE6MIIR%2F20261027%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20261027T024723Z&X-Amz-Expires=600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEBoaCXVzLWVhc3QtMSJIMEYCIQDsk4IeJRCDwvzcwpPsbWP8w%2BsNgXgUlo1ONwja9svbyAIhAIlecvLv0NhSUekGgG1kjYGZN41q6LEWcoy0ajTfO3TIKrAFCOL%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQARoMNjk5NzUzMzA5NzA1IgyVANeu7JlDnVMmGDMqhAVI4zp19Ya7FFYhno%2FllT4paoER4OTQp5nC0CeU8Lr5J%2FJ6uUf%2FWdOy99wlRZo2xTIdxH%2FpT88zK2VT7RvlwTg4F0Z%2BvRW4eB3mqH0owVTNyxRBxGgok%2FABDujy0PODCkRa3cPIhOcuWDGRPMWohqtxLvL9sovLmpW7SOPBmJO9xlPF8AW6z5UWvAoZBCgcJEIKYnrtSst0PIBPyG2%2F1b%2BhN%2BNMbFChOOOUalnj8ixxCJ6WisTo3uXRPRUDi4e%2F7MesOLP8sqZa4glm5tMonz%2B3zFOPlx67t3qs487Ne5517NXsJlwBnr1UYCOm3MM2RlFZpL9CXdGtuKMX4dtkBA1wbbShnNflxs7Y7MB5zXNJ9bEBG6Sw9bX5Ccuf0xIv%2BKnKRlDzkUQLY0KHCW7p7bHeBsYwqxjIwJgnYcAa5NPPhyX%2FVAR1xF4sYmPmaEy4Wxgn2NJYg2wcEiPYTTgltfdFUSaY%2F5SpjNYzEKRr%2FHiXdwxYEyX05hO8FbQptsFB6nUK65uJ1%2F67OJOBwxV2PNmviVYUG7w3hpQP7Ci9pqtysknLHQwMIVCkxoFexSSuLhRrCRx%2BaW0mkfvq95X7Q3UQFGHExxHBx9xYKQ5l%2F6fRMmJIZ0Xt3gms5rL%2B6jG0Fvxhc%2FIVhDDTary3belo11Qrl2X2UsqAipmtlKUpFXPiZkiL04%2FGoMnEtqFWEcvg3QeHkk9CfyD%2BB35uB%2ByX8vLuRbLFA%2Bq3bX8avK9gxQdbL9G4978k6rurJI5Om%2FWSJpBa4lz2G1vB7zGUjCNO6KSIcMQ6cg32dgFztpxFpgalwNcr7T4M75g9vPy0FywIqttzGZyw7NHGOvhC2WLvC%2Fzu361eGjDRjIDXBjqPAXhhRahFwnWtDwg5r1%2FmHTw2x6clSyf5A6%2FoyQv2GkSjWjyJCoxJvP1cf%2B%2B4NlcglVxBspUCZUpn9q7zOxbyx0tLe7fRRTnshkPAdU1CoIxYLVtKTnqdWd6%2FcZTsYv21Xz%2BGRDNkC%2BjcoWwjchKv2uFRzp3qaGf3J18L6mOGQjcPQUGpd0LCROKelwdHlvCw&X-Amz-SignedHeaders=host&response-content-type=text%2Fmarkdown%3B%20charset%3Dutf-8&x-id=GetObject&X-Amz-Signature=a4e12dfc00bb20e1f8c703541b783c7f6bb7dc25c32225e13c6a35b20dd22383)

Cada rodada documentará sementes, fontes consultadas, candidatos, decisões e novos estudos incluídos.

## 16. Síntese e análise de lacunas

A síntese principal será narrativa e tabular, organizada por:

1. Problema clínico e decisão apoiada.
2. Representação dos dados.
3. Formulação de otimização.
4. Arquitetura IA–PO.
5. Incerteza e restrições.
6. Tipo e qualidade da evidência.
7. Resultados, limitações e transferibilidade.

Será construída uma matriz de evidências cruzando os estudos com componentes como pedigree, Knowledge Graph, GNN, aquisição de informação, otimização, decisão sequencial, custo, equidade, validação externa e avaliação prospectiva.

A presença de muitos componentes não será interpretada como superioridade. A matriz servirá para identificar quais combinações foram efetivamente avaliadas e com que evidência.

As possíveis lacunas serão classificadas como:

- De aplicação: método existente ainda não avaliado no domínio.
- De modelagem: aspectos relevantes do problema não formalizados.
- De aprendizado: treinamento preditivo desalinhado da decisão.
- De dados: informações insuficientes ou pouco representativas.
- De avaliação: falta de baselines, robustez ou validação adequada.
- De implementação: ausência de viabilidade, governança ou integração ao serviço.
- De método: limitação algorítmica que exige uma nova abordagem.

Essas categorias dialogam com as hipóteses atuais do projeto sobre aquisição de informação com custos, seleção sob orçamento, restrições explícitas e decisão sequencial, mas sua confirmação dependerá dos textos completos e do corpus final. [pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws](https://pplxfilegitgateway-projectfiles-prod-use1.s3.us-east-1.amazonaws.com/projectfiles-prod/gateway-object-store/repos/files-a5f14286da803e72c73e2980894fde18/downloads/82fdb075169cc7dcfab31dad3221050e54cd9ada/themes.md?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Checksum-Mode=ENABLED&X-Amz-Credential=ASIA2F3EMEYETJE6MIIR%2F20261027%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20261027T024723Z&X-Amz-Expires=600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEBoaCXVzLWVhc3QtMSJIMEYCIQDsk4IeJRCDwvzcwpPsbWP8w%2BsNgXgUlo1ONwja9svbyAIhAIlecvLv0NhSUekGgG1kjYGZN41q6LEWcoy0ajTfO3TIKrAFCOL%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQARoMNjk5NzUzMzA5NzA1IgyVANeu7JlDnVMmGDMqhAVI4zp19Ya7FFYhno%2FllT4paoER4OTQp5nC0CeU8Lr5J%2FJ6uUf%2FWdOy99wlRZo2xTIdxH%2FpT88zK2VT7RvlwTg4F0Z%2BvRW4eB3mqH0owVTNyxRBxGgok%2FABDujy0PODCkRa3cPIhOcuWDGRPMWohqtxLvL9sovLmpW7SOPBmJO9xlPF8AW6z5UWvAoZBCgcJEIKYnrtSst0PIBPyG2%2F1b%2BhN%2BNMbFChOOOUalnj8ixxCJ6WisTo3uXRPRUDi4e%2F7MesOLP8sqZa4glm5tMonz%2B3zFOPlx67t3qs487Ne5517NXsJlwBnr1UYCOm3MM2RlFZpL9CXdGtuKMX4dtkBA1wbbShnNflxs7Y7MB5zXNJ9bEBG6Sw9bX5Ccuf0xIv%2BKnKRlDzkUQLY0KHCW7p7bHeBsYwqxjIwJgnYcAa5NPPhyX%2FVAR1xF4sYmPmaEy4Wxgn2NJYg2wcEiPYTTgltfdFUSaY%2F5SpjNYzEKRr%2FHiXdwxYEyX05hO8FbQptsFB6nUK65uJ1%2F67OJOBwxV2PNmviVYUG7w3hpQP7Ci9pqtysknLHQwMIVCkxoFexSSuLhRrCRx%2BaW0mkfvq95X7Q3UQFGHExxHBx9xYKQ5l%2F6fRMmJIZ0Xt3gms5rL%2B6jG0Fvxhc%2FIVhDDTary3belo11Qrl2X2UsqAipmtlKUpFXPiZkiL04%2FGoMnEtqFWEcvg3QeHkk9CfyD%2BB35uB%2ByX8vLuRbLFA%2Bq3bX8avK9gxQdbL9G4978k6rurJI5Om%2FWSJpBa4lz2G1vB7zGUjCNO6KSIcMQ6cg32dgFztpxFpgalwNcr7T4M75g9vPy0FywIqttzGZyw7NHGOvhC2WLvC%2Fzu361eGjDRjIDXBjqPAXhhRahFwnWtDwg5r1%2FmHTw2x6clSyf5A6%2FoyQv2GkSjWjyJCoxJvP1cf%2B%2B4NlcglVxBspUCZUpn9q7zOxbyx0tLe7fRRTnshkPAdU1CoIxYLVtKTnqdWd6%2FcZTsYv21Xz%2BGRDNkC%2BjcoWwjchKv2uFRzp3qaGf3J18L6mOGQjcPQUGpd0LCROKelwdHlvCw&X-Amz-SignedHeaders=host&response-content-type=text%2Fmarkdown%3B%20charset%3Dutf-8&x-id=GetObject&X-Amz-Signature=2433f0974710f9c33c1c5db6a1f7df1598beda1aa573415abeef17dc49fa3ad6)

## 17. Produtos e encerramento

A revisão produzirá:

- Protocolo versionado no Parsifal.
- Histórico reproduzível das buscas.
- Base deduplicada e decisões de seleção.
- Fluxo de identificação, triagem, recuperação e inclusão.
- Checklist de qualidade e perfil por estudo.
- Formulário de extração preenchido.
- Taxonomia das integrações IA–PO.
- Mapa de evidências e lacunas.
- Síntese dos requisitos de dados e avaliação para a tese.
- Formulação fundamentada do problema de pesquisa.

A revisão será encerrada após execução das estratégias previstas, avaliação dos registros, conclusão do snowballing e atualização final das buscas. O resultado esperado não é demonstrar antecipadamente que a proposta é inédita, mas estabelecer qual decisão merece ser estudada, quais métodos já a resolvem, onde falham e que contribuição adicional pode ser demonstrada com os dados e recursos disponíveis.