# Regras de escopo do projeto TCC

Este documento define as regras de escopo do projeto e deve orientar futuras implementações, revisões e decisões técnicas. Os itens abaixo registram o escopo acordado: funcionalidades consideradas implementadas, entregas pendentes e itens que não são exigidos nesta etapa.

## O que implementamos por estar solicitado no MD

Os itens desta seção são considerados atendidos no escopo do projeto e devem ser preservados nas próximas alterações.

- Experimento com Regressão Logística, Árvore de Decisão e Random Forest.
- Comparação entre SMOTE, peso de classe e nenhum balanceamento.
- Comparação entre dados brutos e tratados.
- Divisão estratificada em treino e teste.
- Remoção automática de identificadores.
- Tratamento de duplicatas e valores inválidos.
- Métricas, matriz de confusão, curvas ROC/PR e importância das variáveis.
- Seleção correta do modelo e do limiar sem usar o conjunto de teste.
- Preparação genérica para CSV, XLS e XLSX.
- IA generativa por sinistro com Ollama.
- Evidências locais, persistência na camada Gold e exibição no dashboard.
- Fallback quando a IA generativa estiver indisponível.

## O que ainda vamos implementar

Os itens desta seção são requisitos pendentes do dashboard oficial em Angular.

- Gráficos no dashboard.
- Distribuição por nível de risco.
- Evolução temporal das análises.
- Fraudes previstas versus confirmadas.
- Métricas do modelo ativo.
- Matriz de confusão no dashboard quando houver rótulos.
- Ranking ou distribuição por score.

## O que não precisa ser implementado

Os itens desta seção estão fora do escopo exigido nesta etapa. Não devem ser tratados como pendências ou adicionados às entregas obrigatórias sem uma revisão explícita destas regras.

- Implementação de nginx.
- Streamlit e Power BI, pois o dashboard oficial é Angular.
- SMOTE no modelo de produção; seu uso ficará restrito ao experimento.
- Regressão Logística e Árvore de Decisão em produção; serão utilizadas apenas como baselines.
- Treinamento diretamente pela camada Silver; o fluxo por upload já atende ao requisito.
- Remoção manual de `PolicyNumber` e `RepNumber`; a remoção de identificadores já é automática.
- SHAP nesta etapa; as evidências locais atendem à primeira versão.
- Versionamento de arquivos compilados de `fraud-dashboard/dist/`.

## Aplicação das regras

- Usar este documento como referência de escopo ao planejar e executar alterações no projeto.
- Priorizar as entregas da seção de implementações pendentes, preservando as funcionalidades consideradas atendidas.
- Manter o conjunto de teste fora da seleção do modelo e do limiar.
- Manter SMOTE no experimento e Regressão Logística e Árvore de Decisão apenas como baselines.
- Usar Angular como dashboard oficial e manter o fallback para indisponibilidade da IA generativa.
- Não versionar os arquivos compilados de `fraud-dashboard/dist/`.
- Atualizar este documento quando houver uma mudança explícita no escopo acordado.
