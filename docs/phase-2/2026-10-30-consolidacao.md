# Possível temática de doutorado

## Aprendizado orientado à decisão e otimização em Knowledge Graphs familiares para priorizar rastreamento genético em cascata sob restrições clínicas, éticas e de recursos

A temática proposta consiste no desenvolvimento de um arcabouço que integre Inteligência Artificial e Pesquisa Operacional para apoiar o planejamento do rastreamento genético em cascata em câncer hereditário. Sua ideia central é utilizar representações relacionais de dados genéticos, clínicos e familiares para estimar informações relevantes e, a partir delas, otimizar decisões sobre priorização de testes e aquisição de informações. A contribuição pretendida vai além de prever quais familiares apresentam maior probabilidade de portar uma variante: busca investigar como aprender e decidir conjuntamente, considerando incerteza, capacidade operacional, custos e limites éticos.

O rastreamento genético em cascata oferece um problema motivador concreto, pois envolve familiares potencialmente elegíveis para investigação após a identificação de uma variante patogênica ou provavelmente patogênica em um probando. Sua implementação depende não apenas de risco genético, mas também de comunicação, acesso, adesão e organização dos serviços. Revisões sobre o tema examinam justamente essas barreiras e as diferenças entre estratégias de comunicação mediadas pelo paciente e contato direto com familiares. [nature](https://www.nature.com/articles/s41525-024-00412-0)

Nesse contexto, o problema de pesquisa pode ser formulado da seguinte maneira: dado um conjunto de famílias com informações genéticas e clínicas parcialmente disponíveis, como selecionar e sequenciar ações de investigação para maximizar o benefício esperado do rastreamento, respeitando restrições clínicas, éticas e de recursos? Essas ações podem incluir a revisão de dados já existentes, o preenchimento de lacunas no histórico familiar e a priorização de familiares para avaliação por uma equipe habilitada. A priorização computacional não substituiria a indicação clínica nem autorizaria contatos ou testes autônomos.

## Representação do problema em grafos familiares

A infraestrutura conceitual da proposta seria um Knowledge Graph capaz de representar pessoas, variantes, genes, exames, condições clínicas e evidências, juntamente com suas relações. Essa estrutura permitiria distinguir parentesco documentado, resultados laboratoriais observados, evidências externas e informações ainda incertas. A temporalidade e a proveniência seriam importantes para identificar quais dados estavam efetivamente disponíveis em cada momento de decisão.

O vínculo com o OncoGeneGraph-BR está na possibilidade de utilizar a estruturação dos dados genético-laboratoriais e familiares como base para uma investigação metodológica em otimização e IA. Nas notas do projeto, a testagem em cascata já aparece como uma oportunidade para selecionar familiares sob orçamento, com possível extensão de uma decisão estática para decisões sequenciais. Entretanto, sua originalidade ainda é uma hipótese a ser verificada na literatura. [themes](themes.md)

Sobre essa representação, modelos estatísticos, métodos de inferência em pedigrees ou GNNs poderiam estimar probabilidades e outras quantidades relevantes. Entre elas estariam a probabilidade de um familiar portar determinada variante, a probabilidade de completar a investigação e o valor esperado de obter uma informação adicional. O uso de GNNs seria uma hipótese metodológica, e não uma condição obrigatória: sua utilidade precisaria ser demonstrada em comparação com alternativas mais simples e com modelos baseados no conhecimento genético disponível.

Também seria necessário separar claramente o que foi observado do que foi inferido. Uma relação familiar predita, por exemplo, não deveria ser tratada como parentesco confirmado. A qualidade e a utilidade das inferências dependeriam de validação compatível com o uso pretendido.

## Integração entre Inteligência Artificial e Pesquisa Operacional

A proposta admite uma evolução em três níveis. No primeiro, uma arquitetura predict-then-optimize utilizaria modelos preditivos para estimar parâmetros que alimentariam um modelo de otimização. A IA estimaria características do problema; a Pesquisa Operacional escolheria ações viáveis diante dessas estimativas. Essa arquitetura permitiria construir uma referência inicial transparente e analisar separadamente os erros de previsão e as limitações da decisão.

No segundo nível, a otimização incorporaria explicitamente incerteza e atualização de informações. O resultado de um teste ou o esclarecimento de um vínculo familiar poderia alterar as decisões seguintes. Dependendo da estrutura e da disponibilidade dos dados, o problema poderia ser tratado por programação estocástica, otimização robusta, programação dinâmica ou modelos de decisão sequencial. A escolha entre esses métodos precisaria decorrer do problema observado, evitando adotar uma formulação complexa sem necessidade.

No terceiro nível estaria o principal candidato à contribuição metodológica: o **aprendizado orientado à decisão**. Nesse paradigma, o modelo não seria treinado apenas para produzir previsões próximas dos valores observados, mas também para melhorar as decisões produzidas pelo sistema de otimização. A literatura de decision-focused learning investiga justamente a integração entre modelos aprendidos e problemas decisórios, levando em conta a perda associada à decisão final. [arxiv](https://arxiv.org/abs/2307.13565)

Essa distinção é relevante porque erros preditivos semelhantes podem ter consequências operacionais diferentes. Uma alteração em uma probabilidade pode não mudar a seleção de familiares em determinado cenário, mas pode modificar substancialmente a alocação de recursos em outro. A pesquisa investigaria, portanto, quando a melhoria da previsão se traduz em melhoria da decisão e quando seria mais adequado orientar o treinamento diretamente por esse objetivo.

## Aquisição de informação como extensão do problema

Uma extensão particularmente coerente seria integrar a priorização de ações de rastreamento à escolha de quais informações obter primeiro. Em um pedigree incompleto, o sistema poderia enfrentar duas alternativas: agir com base no conhecimento atual ou investir parte dos recursos para reduzir uma incerteza relevante.

Isso aproxima a proposta de active learning, valor da informação e desenho ótimo de experimentos. No entanto, seria importante distinguir dois objetivos: adquirir informações para melhorar o modelo de IA e adquirir informações para melhorar a decisão referente a uma família. Esses objetivos podem coincidir, mas também podem competir.

As notas do projeto já identificam a seleção de informações sob custos heterogêneos como uma possível contribuição: em vez de assumir um número fixo de consultas ou rótulos, considerar o custo de cada ação e o ganho esperado. A disponibilidade desses custos e a possibilidade de estimar os ganhos são riscos que exigiriam avaliação em um piloto. [themes](themes.md)

Essa extensão ampliaria a tese sem abandonar sua unidade: o mesmo arcabouço passaria a decidir tanto como utilizar o conhecimento disponível quanto onde investir para obter conhecimento adicional.

## Objetivos e restrições da decisão

A função objetivo não deveria ser definida apenas por conveniência matemática. Ela precisaria refletir uma finalidade acordada com os profissionais e gestores envolvidos. Possíveis objetivos incluem aumentar a identificação de portadores entre familiares elegíveis, ampliar cobertura, reduzir tempo até a investigação ou melhorar a utilização dos recursos disponíveis.

Essas finalidades não são equivalentes. Maximizar o número esperado de resultados positivos pode favorecer pessoas mais acessíveis e deixar de lado grupos com barreiras de acesso. Da mesma forma, ganho informacional não significa necessariamente benefício clínico imediato. A formulação deveria tornar esses conflitos explícitos, por meio de restrições, análises de cenários ou objetivos múltiplos.

As restrições poderiam envolver orçamento, capacidade laboratorial, disponibilidade de aconselhamento, elegibilidade clínica, sequência das ações e consentimento. Aspectos como privacidade e legitimidade do contato não seriam tratados apenas como termos penalizáveis de uma função objetivo: determinadas ações simplesmente não poderiam integrar o conjunto de alternativas permitidas.

O sistema seria, assim, uma ferramenta de apoio à análise e ao planejamento, com supervisão humana e rastreabilidade. Sua avaliação deveria examinar não apenas qual ação foi sugerida, mas também quais evidências, pressupostos e restrições levaram a essa sugestão.

## Possíveis contribuições científicas

A contribuição central poderia assumir a forma de uma metodologia de aprendizado e decisão em grafos parcialmente observados, motivada pelo rastreamento familiar. As contribuições específicas dependeriam do resultado da revisão e da viabilidade dos dados, mas poderiam incluir:

- Uma formulação de otimização para seleção e sequenciamento de ações em grafos familiares.
- Um método de integração entre modelos relacionais e otimização, comparando treinamento preditivo convencional com treinamento orientado à decisão.
- Uma estratégia de aquisição de informação que considere custos, incerteza e efeito sobre decisões posteriores.
- Um protocolo de avaliação que separe desempenho preditivo, qualidade decisória e benefício assistencial.
- Uma análise das condições em que a complexidade adicional de GNNs ou de treinamento integrado produz vantagem sobre alternativas mais simples.

Esparsificação do grafo, otimização multiobjetivo e explicabilidade poderiam apoiar essas contribuições, mas não precisariam constituir linhas independentes. Nas notas atuais, a otimização multiobjetivo e a seleção de subgrafos aparecem como temas relacionados, com diferentes níveis de evidência e risco de sobreposição com trabalhos existentes. [themes](themes.md)

GraphRAG, por sua vez, poderia funcionar como interface de consulta e recuperação de evidências, mas não seria necessário para demonstrar a contribuição principal em aprendizado e otimização.

## Estratégia de avaliação

A avaliação deveria começar com uma pergunta operacional bem delimitada e referências simples. Antes de investigar modelos integrados complexos, seria necessário verificar se o problema pode ser resolvido satisfatoriamente por critérios clínicos, probabilidades mendelianas, heurísticas ou otimização alimentada por modelos convencionais.

A comparação incluiria, conforme aplicável, estratégias baseadas em risco, políticas simples, modelos predict-then-optimize e métodos orientados à decisão. Em instâncias pequenas, soluções exatas poderiam fornecer referências para avaliar a qualidade dos métodos aproximados.

As métricas deveriam acompanhar os níveis de alegação. Desempenho preditivo envolveria discriminação e calibração; desempenho decisório envolveria utilidade, viabilidade, custo, qualidade da solução e sensibilidade aos erros; desempenho operacional envolveria cobertura, capacidade e tempo. Benefício clínico exigiria evidência específica, não podendo ser deduzido exclusivamente de AUC elevada ou de resultados de simulação.

A validação também deveria distinguir cenários como novos familiares de famílias conhecidas e famílias inteiramente novas. Resultados em um cenário não seriam automaticamente generalizados para o outro. Dados ausentes, viés de encaminhamento e diferenças entre a população testada e a população elegível precisariam integrar a análise crítica.

## Viabilidade, limites e delimitação da tese

A viabilidade dependerá de informações que precisam ser verificadas: qualidade dos pedigrees, quantidade de famílias utilizáveis, disponibilidade de resultados, registro de elegibilidade, custos, capacidade e trajetórias de investigação. Conhecer apenas quem realizou o teste pode ser insuficiente para avaliar políticas de priorização, pois não revela necessariamente quem poderia ter sido testado ou por que determinadas ações ocorreram.

Por isso, a pesquisa poderia avançar em etapas: caracterização dos dados e da decisão; construção de baselines; formulação de otimização; integração com aprendizado; e extensão para aquisição sequencial de informação. Caso os dados não sustentem uma avaliação clínica completa, estudos controlados com instâncias sintéticas e dados retrospectivos poderiam apoiar a investigação metodológica, mantendo explícitos seus limites.

Para preservar o escopo, a tese deveria priorizar um problema decisório, uma família de objetivos e uma contribuição metodológica principal. Integrar todos os componentes discutidos não deve ser uma exigência. A amplitude científica viria da profundidade da integração e da avaliação, não do número de tecnologias utilizadas.

## Síntese da proposta

A possibilidade de temática pode ser expressa como o desenvolvimento e a avaliação de métodos que aprendam representações e estimativas em grafos familiares para melhorar decisões de rastreamento genético sob restrições. O câncer hereditário forneceria o problema motivador e os requisitos de avaliação; a contribuição em Ciência da Computação estaria na integração entre aprendizado, aquisição de informação e otimização.

A pergunta central seria: em quais condições aprender considerando a decisão final permite utilizar melhor informações e recursos do que prever e otimizar separadamente?

Essa formulação mantém a ambição de gerar métodos relevantes para IA, sem presumir que GNNs sejam necessárias, que a integração seja inédita ou que ganhos computacionais impliquem benefício clínico. A originalidade deverá resultar da comparação com a literatura e da identificação de uma limitação concreta que o método proposto consiga superar.