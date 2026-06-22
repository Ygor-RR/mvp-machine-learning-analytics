# MVP — Predição de Churn em Telecomunicações

Aluno: Ygor Ribeiro Rodrigues
Curso: Machine Learning & Analytics
Instituição: PUC-Rio

📌 Sobre o projeto
MVP de Machine Learning desenvolvido para prever o cancelamento de clientes (churn) em uma empresa de telecomunicações.

O objetivo é identificar clientes com maior probabilidade de cancelamento, permitindo apoiar estratégias de retenção e tomada de decisão baseada em dados.

🎯 Tipo de problema
Classificação supervisionada binária.

Variável-alvo: Churn

Yes: cliente cancelou o serviço
No: cliente permaneceu ativo

📊 Dataset
Nome: Telco Customer Churn
Fonte: Kaggle
Registros: 7.043
Atributos originais: 21

O dataset foi carregado por URL pública, garantindo reprodutibilidade e dispensando upload manual, login, API key ou configuração local.

🧪 Etapas do projeto
O notebook segue o fluxo completo de um projeto de Machine Learning:

Definição do problema
Apresentação do dataset
Análise exploratória dos dados
Preparação dos dados
Divisão treino/teste
Construção de pipelines
Treinamento de modelos
Otimização de hiperparâmetros
Avaliação dos resultados
Conclusão crítica do MVP

🤖 Modelos avaliados
Foram avaliados os seguintes modelos:

DummyClassifier como baseline
Regressão Logística
Random Forest
XGBoost otimizado
Resultados no conjunto de teste:

DummyClassifier: F1-Score = 0.0000
Regressão Logística: F1-Score = 0.6040
Random Forest: F1-Score = 0.5321
XGBoost otimizado: F1-Score = 0.5882

🏆 Melhor modelo
O melhor modelo foi a Regressão Logística, com:

F1-Score no teste: 0.6040
Hiperparâmetros principais:
C=1.0
class_weight='balanced'
A Regressão Logística foi selecionada por apresentar o maior F1-Score, métrica principal definida para este MVP, além de demonstrar boa capacidade de generalização.

⚙️ Principais tratamentos realizados
Durante a preparação dos dados foram aplicados:

Remoção da coluna customerID, por ser apenas um identificador único
Conversão da variável-alvo Churn para formato numérico
Conversão de TotalCharges para numérico dentro do pipeline
Imputação de valores ausentes com mediana dentro do pipeline
Padronização das variáveis numéricas com StandardScaler
Codificação das variáveis categóricas com OneHotEncoder
Uso de Pipeline e ColumnTransformer para evitar vazamento de dados

📈 Métrica principal
A métrica principal escolhida foi o F1-Score, por equilibrar:

Precisão
Recall
Essa escolha é adequada porque o problema apresenta desbalanceamento moderado entre as classes.

▶️ Como executar
Abra o notebook no Google Colab.
Execute todas as células em ordem.
O dataset será carregado automaticamente por URL pública.
Não é necessário upload manual ou configuração local.

📁 Arquivos do repositório
MVP_YgorRodrigues.ipynb: notebook principal do projeto
WA_Fn-UseC_-Telco-Customer-Churn.csv: dataset utilizado
README.md: descrição resumida do projeto

✅ Conclusão
O MVP atingiu seu objetivo ao construir uma solução completa, reproduzível e documentada para previsão de churn em telecomunicações.

A Regressão Logística apresentou o melhor desempenho segundo a métrica principal definida, enquanto o XGBoost obteve bons resultados em Accuracy e ROC-AUC. Como próximos passos, poderiam ser exploradas técnicas de balanceamento, novas variáveis e ajustes adicionais de hiperparâmetros.
