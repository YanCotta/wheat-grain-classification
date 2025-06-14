# 🌾 Classificação de Grãos de Trigo com Machine Learning

## 📖 Descrição do Projeto

Este projeto universitário aplica a metodologia **CRISP-DM** para desenvolver e avaliar um modelo de Machine Learning capaz de classificar três variedades de grãos de trigo (Kama, Rosa e Canadian) com base em suas características físicas. O objetivo é automatizar o processo de classificação, que em pequenas cooperativas agrícolas é frequentemente manual, demorado e sujeito a erros.

A solução proposta visa aumentar a eficiência e a precisão da classificação de grãos, fornecendo uma ferramenta robusta baseada em dados.

---

## 🛠️ Metodologia Utilizada: CRISP-DM

O projeto está estruturado em torno das fases do **CRISP-DM (Cross-Industry Standard Process for Data Mining)**, garantindo uma abordagem organizada e iterativa:

1.  **Business Understanding:** Definição do problema e dos objetivos de negócio.
2.  **Data Understanding:** Análise exploratória para se familiarizar com o dataset.
3.  **Data Preparation:** Limpeza, transformação e preparação dos dados para a modelagem.
4.  **Modeling:** Implementação e comparação de diferentes algoritmos de classificação.
5.  **Evaluation:** Avaliação do desempenho dos modelos e otimização de hiperparâmetros.
6.  **Deployment:** Interpretação dos resultados finais e extração de insights para o negócio.

---

## 📊 Dataset

Utilizamos o **"Seeds Dataset"**, disponível publicamente no [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/236/seeds).

O conjunto de dados contém 210 amostras com 7 atributos geométricos:
* Área
* Perímetro
* Compacidade
* Comprimento do Núcleo
* Largura do Núcleo
* Coeficiente de Assimetria
* Comprimento do Sulco do Núcleo

A variável alvo é a **variedade** do trigo, com 3 classes distintas.

---

## 🚀 Como Executar o Projeto

Para executar o notebook e replicar os resultados, siga os passos abaixo.

**1. Clone o Repositório:**
```bash
git clone [https://github.com/SEU-USUARIO/wheat-grain-classification.git](https://github.com/SEU-USUARIO/wheat-grain-classification.git)
cd wheat-grain-classification
2. Crie e Ative um Ambiente Virtual (Recomendado):

Bash

python -m venv venv
source venv/bin/activate  # No Windows, use: venv\Scripts\activate
3. Instale as Dependências:
As bibliotecas necessárias estão listadas no arquivo requirements.txt.

Bash

pip install -r requirements.txt
(Observação: Se o arquivo requirements.txt não existir, você pode criá-lo com o conteúdo abaixo ou instalar as bibliotecas manualmente: pip install pandas numpy matplotlib seaborn scikit-learn jupyterlab)

Conteúdo para requirements.txt:

pandas
numpy
matplotlib
seaborn
scikit-learn
jupyterlab
4. Execute o Jupyter Notebook:

Bash

jupyter lab grain_classification.ipynb
Após abrir o notebook, você pode executar todas as células para ver o processo de análise, treinamento e avaliação dos modelos.

📈 Resultados Esperados
O projeto culmina na entrega de um modelo de classificação otimizado, capaz de distinguir as variedades de trigo com alta acurácia. A análise final inclui:

Uma comparação de desempenho entre múltiplos algoritmos (KNN, SVM, Random Forest, etc.).
A identificação das características mais importantes para a classificação.
Uma interpretação clara dos resultados, conectando as métricas técnicas aos objetivos do problema.