# Plano de revisão da parte escrita do TCC

## Objetivo e prazo

Reformular e concluir a parte escrita para representar com precisão o sistema desenvolvido e o estudo realizado, seguindo o modelo do professor.

Prazo informado pelo usuário: **10 de novembro de 2026**. Este plano foi iniciado em 8 de outubro de 2026. As etapas abaixo são uma proposta de organização do trabalho, não novos prazos exigidos pelo professor.

Documento de trabalho: [tcc.docx](tcc.docx). Referência de estrutura e formatação: [template-professor.docx](template-professor.docx). Branch de trabalho: `homolog`.

## Diagnóstico inicial

Esta é uma conferência inicial de trechos do documento, da documentação técnica e de arquivos da implementação. Ainda não representa uma auditoria integral da bibliografia, da formatação ou da execução do sistema.

| Trecho ou tema | Problema encontrado | Revisão necessária |
| --- | --- | --- |
| Seção 1.4, Metodologia | O texto menciona aprendizado não supervisionado e, na mesma descrição, justifica classificação supervisionada. | Distinguir a classificação de fraude em bases rotuladas da detecção de anomalias em bases sem rótulo, conforme o procedimento efetivamente usado no estudo. |
| Seção 3.1.1, Linguagens e bibliotecas | Atribui a construção do dashboard ao Streamlit, enquanto outras seções descrevem Angular e o frontend atual depende de Angular. | Unificar a descrição das tecnologias e suas responsabilidades. |
| Seção 3.2.8, Treinamento e validação | Descreve treinamento pela camada Silver com SMOTE. O serviço de treinamento consultado lê um dataset por arquivo e a estratégia supervisionada usa Random Forest com peso de classe, sem SMOTE nesse fluxo. | Separar experimento acadêmico, treinamento de candidatos e inferência operacional. Documentar SMOTE apenas onde seu uso estiver comprovado. |
| Resultados, discussão e conclusão | Na estrutura de títulos extraída do documento, o capítulo 3 é seguido pelas referências, sem os capítulos 4, 5 e 6 anunciados na introdução. | Escrever esses capítulos a partir de evidências do estudo e das limitações verificadas. |
| Elementos iniciais | Resumo e abstract aparecem como títulos sem conteúdo na extração. | Redigir após consolidar método, resultados e conclusão. |
| Referências | Há entradas bibliográficas repetidas, incluindo CNSEG, Hanzawa e Leal. | Deduplicar, conferir correspondência entre citações e referências e verificar as fontes antes de corrigir seus dados. |

Fontes técnicas consultadas na branch `homolog`:

- [README do sistema](../../README.md).
- [Regras de escopo](../REGRAS_DO_PROJETO.md).
- [Serviço de treinamento](../../ml-fraud-py/fraud_detection/application/training.py).
- [Estratégia de treinamento supervisionado](../../ml-fraud-py/fraud_detection/training/supervised.py).
- [Dependências do frontend](../../fraud-dashboard/package.json).

As regras de escopo registram itens como implementados que precisam de conferência específica no código e nas evidências experimentais. Esse registro, isoladamente, não comprova execução, desempenho ou resultados científicos. Divergências devem ser esclarecidas antes de virar afirmações no TCC.

## Ordem de trabalho

1. **Conferir método e evidências.** Mapear funcionalidades, fluxos, datasets, experimentos e arquivos de resultados realmente disponíveis. Distinguir itens implementados, planejados e efetivamente testados.
2. **Reformular o capítulo 3.** Atualizar materiais, arquitetura, ingestão, tratamento, treinamento, validação, inferência, dashboard e papel da IA generativa. Definir um procedimento experimental reproduzível.
3. **Alinhar introdução e objetivos.** Ajustar pergunta de pesquisa, objetivo geral, objetivos específicos e síntese da metodologia ao estudo efetivamente realizado.
4. **Concluir resultados e discussão.** Apresentar métricas, tabelas e figuras obtidas em execuções documentadas. Discutir falsos positivos, falsos negativos, desbalanceamento, limites da base e contribuição do tratamento dos dados. Não afirmar melhoria antes de demonstrá-la.
5. **Escrever conclusão, resumo e abstract.** Responder à pergunta de pesquisa com base nos resultados e explicitar limitações e trabalhos futuros.
6. **Revisar literatura, referências e formatação.** Verificar fontes, remover duplicidades, atualizar figuras e tabelas, conferir sumário e inspecionar o documento renderizado conforme o modelo do professor.

## Critérios para concluir

- Texto coerente com a versão do sistema utilizada no estudo.
- Método reproduzível e evidências identificáveis para os resultados apresentados.
- Conclusões proporcionais às evidências, sem afirmar que um score confirma fraude.
- Citações e referências conferidas, sem fontes ou resultados inventados.
- Capítulos e elementos acadêmicos necessários preenchidos conforme o modelo e as orientações do professor.
- DOCX renderizado e revisado visualmente, com revisão final antes de 10 de novembro de 2026.

## Estado atual

Diagnóstico inicial registrado. A reformulação do conteúdo do DOCX ainda não foi executada. A próxima etapa é conferir os detalhes do método e as evidências disponíveis para fundamentar a revisão do capítulo 3.
