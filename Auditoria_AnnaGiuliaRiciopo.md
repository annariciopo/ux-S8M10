# Auditoria do Plano de DesignOps: Framework REACH

## Parte 1: Triangulação de Eficiência e Habilidade (Efficiency & Ability)

A métrica de **Eficiência** serve para avaliar se conseguimos tirar os obstáculos do caminho para que o time produza sem interrupções. A métrica de **Habilidade** mede se a equipe realmente tem o tempo e as condições necessárias para cumprir os processos que foram combinados no papel. No nosso planejamento inicial, definimos o ritual de **Revisão Cruzada**, estabelecendo que nenhum código ou alteração visual poderia ser aprovado sem a avaliação prévia de outro colega do grupo.

### O momento em que o processo gerou um gargalo

Esse processo acabou criando um obstáculo real no nosso fluxo de trabalho do dia a dia. Como evidência desse problema, cito o **Merge Request #39** ([https://git.inteli.edu.br/graduacao/2026-1b/t13/g05/-/merge_requests/39](https://git.inteli.edu.br/graduacao/2026-1b/t13/g05/-/merge_requests/39)). Esse código ficou travado na esteira esperando por uma avaliação dos outros integrantes, porém, por ser algo que necessariamente precisava estar na `develop` para ser testado, acabou sendo aprovado pelo mesmo integrante que o criou.

### Análise Crítica e Causa Raiz

A falha não aconteceu por falta de conhecimento técnico da equipe, mas sim porque criamos um processo irrealista para a nossa rotina estudantil. O plano assumia uma dedicação média de 1 hora por dia por integrante. Como todos do grupo estavam sobrecarregados com as demais tarefas e entregas do módulo, pedir revisões de última hora fez com que ninguém tivesse tempo livre imediato para parar e analisar o meu trabalho. Isso gerou um tempo de espera forçado e improdutivo, provando que o processo diminuiu a nossa eficiência real e ignorou a nossa capacidade real de trabalho.

### Solução Prática na Vida Real

Para evitar que o projeto continuasse travando, nós mudamos a nossa organização de trabalho. Em vez de pedir revisões de forma desordenada e em cima da hora, nós implementamos um **sistema de revisões planejadas** logo no início de cada ciclo (sprint). Cada integrante passou a iniciar a semana sabendo exatamente quais tarefas dos colegas ficariam sob sua responsabilidade para revisar. Com essa previsibilidade, todos conseguiram se organizar para encaixar essa atividade no seu tempo livre diário.

---

## Parte 2: O Desafio da Clareza e dos Resultados (Clarity & Results)

A métrica de **Clareza** serve para avaliar se o cliente e o próprio time entendem o valor real e as razões por trás das decisões visuais e de interface. A métrica de **Resultados** mede se a experiência prática realmente melhorou para o usuário final do sistema.

### A Decisão de Interface e a Falha de Registro

Durante o desenvolvimento, nossa equipe projetou e apresentou uma proposta de painel visual (dashboard web) focado em exibir os dados e status das validações dos testes de drone. No entanto, em uma reunião de validação presencial, o parceiro da Jacto Drones relatou que preferia um relatório prático, descritivo e em formato de texto. Para eles, não fazia sentido ter "mais um site" na rotina operacional para monitorar esses dados; um documento direto e detalhado seria muito mais útil.

Como essa conversa e o feedback aconteceram de forma estritamente presencial e ninguém do grupo ficou responsável por fazer uma ata de reunião, nós enfrentamos uma **ausência de evidência documental escrita**. Isso representa uma falha de organização e de governança do nosso próprio plano original.

### Análise Crítica: A Armadilha da Opinião Subjetiva

O nosso plano de DesignOps **falhou em trazer Clareza** para essa decisão. O planejamento se preocupou muito em construir automações e testes voltados para a qualidade interna do código, mas esqueceu de olhar para as necessidades reais do cliente. Nós não realizamos nenhuma pesquisa rápida ou teste com os engenheiros da Jacto antes de começar a desenhar as telas para entender o que eles precisavam.

Sem dados concretos para justificar a escolha por uma interface gráfica, a validação caiu inteiramente na opinião subjetiva e na preferência pessoal do parceiro. A estrutura de DesignOps falhou em provar o **Resultado** dessa mudança para a empresa porque o painel visual complexo foi tratado como um fim em si mesmo. O cliente enxergou a interface visual como um trabalho extra e desnecessário, provando que, no contexto deles, um relatório descritivo em texto simples gerava muito mais valor prático.

---

## Parte 3: A Lente Humana e a Saúde do Time (Health)

No pilar de **Saúde**, avaliamos o bem-estar dos integrantes, a carga de trabalho e se os processos estão gerando estresse ou cansaço excessivo nas pessoas do grupo.

### A Utopia do Planejamento: Métricas de UX via API

Sendo muito sincera e rigorosa na autocrítica do nosso planejamento anterior, a ideia de **rastrear métricas automáticas de UX puxando dados diretamente da API do GitLab** foi totalmente irrealista para a nossa realidade. O plano exigia o uso obrigatório de etiquetas específicas (como `ux` e `problem-report`) para calcular automaticamente gráficos com tempos de aprovação e taxas de erro visuais.

### O Impacto na Saúde Mental e na Carga de Trabalho

Na prática do dia a dia da faculdade, essa exigência acabou se tornando uma burocracia pesada que atrapalhou o desenvolvimento em vez de ajudar. Obrigar o grupo a manter uma organização impecável de etiquetas para alimentar scripts automáticos gerou um estresse desnecessário em um time que já tinha pouco tempo disponível. Isso acabou atrasando as entregas e travando o andamento contínuo do projeto. O tempo que deveríamos gastar melhorando o código ou simplificando os relatórios do drone era desperdiçado tentando fazer a burocracia do plano funcionar, o que aumentou o cansaço mental de todos.

### Os Cortes Pragmáticos Necessários

Para que o DesignOps funcione como um facilitador real e preserve a saúde do time, eu eliminaria os seguintes pontos do plano original:

* **Eliminar o rastreamento automático de métricas de UX via API:** O acompanhamento do progresso visual deve ser feito conversando de forma simples nas reuniões semanais, abolindo scripts automáticos de monitoramento complexos.
* **Reduzir e fundir os rituais síncronos:** Extinguir reuniões separadas focadas apenas em design (Design Sync) e integrar esse assunto rapidamente à reunião diária geral (Daily) do grupo, economizando o tempo útil de todo mundo.
