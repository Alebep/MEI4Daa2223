# Introdução

Este repositório contém o código-fonte do modelo vencedor da competição ML @SBS/DAA - 5ª Edição (2022/2023), a presente competição está relacionada com o Trabalho Prático de Grupo das UCs do perfil Machine Learning: Fundamentos e Aplicações da Uminho e da UC Dados e Aprendizagem Automática, tendo, como destinatários, alunos do Mestrado em Engenharia Informática, do Mestrado em Matemática e Computação, e do Mestrado em Engenharia de Sistemas. 

A modelação de incidentes rodoviários é um conhecido problema de características estocásticas, não-lineares. Tem, contudo, aparecido na literatura um conjunto de modelos que demonstram um potencial assinalável neste tipo de previsões. Com isso em consideração, foi construído um dataset que contém dados referentes à quantidade e características dos incidentes rodoviários que ocorreram na cidade Guimarães em 2021. O objetivo deste trabalho passa por, entre outros, desenvolver
modelos de Machine Learning capazes de prever o nível de incidentes rodoviários, numa determinada hora.

# Conjunto de Dados

O conjunto de dados utilizado neste projeto contém informações detalhadas sobre a quantidade e características dos incidentes rodoviários ocorridos em Guimarães ao longo de 2021. Os dados foram cuidadosamente coletados e pré-processados, levando em consideração as características estocásticas e não-lineares do problema. O processo de pré-processamento envolveu etapas como limpeza, transformação de features e normalização, a fim de garantir a qualidade e a consistência dos dados.

# Metodologia

O desenvolvimento deste projeto seguiu a abordagem CRISP-DM (Cross-Industry Standard Process for Data Mining), uma estrutura amplamente reconhecida e utilizada para orientar o ciclo de vida completo de projetos de mineração de dados e análise preditiva. Através dessa metodologia estruturada, o processo foi dividido em etapas claramente definidas, permitindo uma abordagem sistemática e iterativa para explorar, modelar e prever incidentes rodoviários.

A fim de aplicar esta metodologia baseada em CRISP-DM, foi seguido os
seguintes passos:
* Compreensão do problema proposto e os seus objetivos;
* Obtenção e seleção de dados relevantes para o problema;
* Preparação dos dados: Limpeza, transformação e integração dos dados
para torná-los adequados para analise. Isto incluiu a analise exploratória
dos dados, a limpeza e a transformação dos dados para remover inconsistências e outliers;
* Modelagem: Aplicação de técnicas de aprendizagem automática para construir modelos preditivos. Isto incluiu a seleção de algoritmos, a validação
de modelos e a otimização de parâmetros;
* Avaliação: Avaliar a qualidade dos modelos construídos e escolher o melhor modelo. Isto envolveu a avaliação da precisão e robustez do modelo,
a comparação com modelos alternativos e a seleção do melhor modelo;
* Implantação do modelo escolhido;


# Resultados e Discussão

Na tabela abaixo, temos a lista de algortimos testados:

## Tabela de Resultados

| Algoritmo              | Melhores Hiperparâmetros                                     | Acurácia |
|------------------------|-------------------------------------------------------------|----------|
| LogisticRegression     | 'fit intercept': True, 'max iter': 10, 'penalty': 'l2', 'tol': 0.0001 | 0.41     |
| DecisionTreeClassifier | 'max depth': 1000, 'max features': 'log2', 'min samples leaf': 1, 'min samples split': 2 | 0.89 |
| KNeighborsClassifier   | 'algorithm': 'brute', 'n neighbors': 20, 'p': 1, 'weights': 'distance' | 0.71     |
| RandomForestClassifier | 'criterion': 'entropy', 'max depth': None, 'max features': 1.0, 'n estimators': 100 | 0.94 |
| BaggingClassifier      | 'max features': 1.0, 'max samples': 0.5, 'n estimators': 100, 'random state': None | 0.93     |


Como podemos observar na tabela, obtivemos os melhores resultados com o algoritmo RandomForest. Esse foi o algoritmo que utilizamos para fazer a submissão com os melhores resultados no kaggle. Os resultados obtidos com o RandomForest durante os testes, foram similares aos obtidos no kaggle, o que demonstra que o nosso modelo conseguiu fazer uma boa generalização dos dados. Os testes foram realizados, usando o dataset de treino, e obtivemos 0.94 de acurácia. O resultado obtido no kaggle foi de 0.95857 de acurácia. Na figura 6 podemos observar a leaderboard com o resultado final da competição no kaggle.

## Uso do Código

O código-fonte fornecido neste repositório pode ser utilizado como referência ou ponto de partida para projetos relacionados à previsão de eventos estocásticos em domínios semelhantes. Os notebooks Jupyter contêm etapas detalhadas de pré-processamento, modelagem e avaliação, facilitando a compreensão e a adaptação do fluxo de trabalho.

# Conclusão

Este projeto representa uma exploração significativa no campo da previsão de incidentes rodoviários usando abordagens avançadas de Machine Learning. Através do comprometimento com a qualidade dos dados, metodologias sólidas e análises aprofundadas, este trabalho oferece insights valiosos para a mitigação de riscos rodoviários. Espero que este repositório seja útil e inspire futuras pesquisas e inovações no domínio da análise de dados aplicada à segurança viária.

Sinta-se à vontade para entrar em contato comigo caso tenha alguma dúvida, sugestão ou colaboração.

[Inserir suas informações de contato aqui]

