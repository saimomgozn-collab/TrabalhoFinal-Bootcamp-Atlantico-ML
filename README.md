# TrabalhoFinal-Bootcamp-Atlantico-ML
Implantação Final FOOD-5K

🍔 Food5k Classifier: Automação de Controle de Qualidade Visual

Este projeto utiliza Deep Learning para garantir que nossa vitrine seja sempre apetitosa.

🎯 O Objetivo de Negócio

Em plataformas de delivery, a qualidade visual é crucial para a conversão de vendas. Usuários e restaurantes fazem upload de milhares de imagens diariamente. O desafio é: Como filtrar automaticamente o que é foto de comida real e o que é ruído (recibos, selfies, objetos aleatórios)?

Este projeto implementa um pipeline de Visão Computacional treinado no dataset Food5k para classificar imagens em duas categorias críticas:

Food: Imagens de alimentos (Aptas para o catálogo/feed).

Non-Food: Imagens diversas (Devem ser descartadas ou marcadas para revisão).

O objetivo é reduzir a carga de moderação manual e melhorar a consistência visual da plataforma.

🧠 O Dataset (Food5k)

Utilizei o dataset Food5k, referência para tarefas de classificação binária alimentar.

Total de Imagens: 5.000

Estrutura: Dividido balanceadamente entre classes Food (1) e Non-Food (0).

Desafio: Alta variabilidade intra-classe (ângulos, iluminação e tipos de comida variados).

⚙️ Arquitetura da Solução

O projeto foi desenvolvido no Google Colab utilizando aceleração via GPU (T4) para otimização do tempo de treinamento.

1. Engenharia de Dados & Pipeline

Ingestão Automatizada: Integração direta com a API do Kaggle para download e extração dos dados.

Pré-processamento: Normalização de pixels, redimensionamento de imagens e Data Augmentation (rotação, zoom, flip) para evitar overfitting e aumentar a robustez do modelo.

2. Modelagem (Deep Learning)

Arquitetura: Rede Neural Convolucional (CNN) customizada / Transfer Learning (VGG16/ResNet - Adaptar conforme seu código real).

Otimização: Uso de EarlyStopping e ModelCheckpoint para garantir o melhor estado dos pesos e evitar desperdício computacional.

3. Avaliação de Performance

Não basta acurácia; o foco foi entender os erros do modelo:

Confusion Matrix: Para visualizar falsos positivos (classificar um sapato como comida) e falsos negativos.

Métricas Detalhadas: Análise de Precision, Recall e F1-Score para garantir equilíbrio na detecção.

📊 Resultados e Data Storytelling

O modelo alcançou resultados promissores para implementação em produção:

Métrica

Performance (Validação)

Acurácia

~90%+ (Estimado)

Precisão (Food)

Alta confiabilidade na detecção de alimentos

Recall (Non-Food)

Capacidade robusta de filtrar lixo visual

Os gráficos detalhados de perda (loss) e acurácia durante as épocas de treinamento estão disponíveis no notebook, demonstrando a convergência estável do modelo.

🚀 Como Executar

Este projeto foi desenhado para ser reproduzível.

Clone o repositório:

git clone [https://github.com/seu-usuario/food5k-classifier.git](https://github.com/seu-usuario/food5k-classifier.git)


Abra no Google Colab ou Jupyter Notebook:
Carregue o arquivo Trabalho_Final_Bootcamp_Avanti.ipynb.

Configuração do Kaggle:
Certifique-se de ter seu arquivo kaggle.json pronto para upload na primeira célula de execução.

Execute o Pipeline:
Rode todas as células para baixar o dataset, treinar o modelo e visualizar os resultados.

🛠 Stack Tecnológico

Linguagem: Python

Deep Learning: TensorFlow / Keras

Manipulação de Dados: Pandas, NumPy

Visualização: Matplotlib, Seaborn

Ambiente: Google Colab (GPU T4)

👨‍💻 Autor

Saimom Goz Siebem

Estudante de Ciência da Computação & Especialista em Machine Learning
