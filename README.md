# 🌾 Classificação de Grãos de Trigo com Machine Learning

## 📖 Descrição do Projeto

Este projeto universitário aplica a metodologia **CRISP-DM** para desenvolver e avaliar um modelo de Machine Learning capaz de classificar três variedades de grãos de trigo (Kama, Rosa e Canadian) com base em suas características físicas. O objetivo é automatizar o processo de classificação, que em pequenas cooperativas agrícolas é frequentemente manual, demorado e sujeito a erros.

A solução proposta visa aumentar a eficiência e a precisão da classificação de grãos, fornecendo uma ferramenta robusta baseada em dados.

## 🎯 Principais Descobertas e Resultados

### 📊 Qualidade Excepcional dos Dados
- **Dataset completo:** 0 valores ausentes em todas as 210 amostras
- **Balanceamento perfeito:** 70 amostras para cada uma das 3 variedades
- **Alta qualidade:** Dados limpos e prontos para análise, sem necessidade de técnicas de imputação

### 🔍 Insights da Análise Exploratória
- **Excelente separabilidade:** As três variedades apresentam clusters distintos e bem definidos
- **Correlações fortes:** Características geométricas altamente correlacionadas (área ↔ perímetro: r=0.99)
- **Características distintivas:** asymmetry_coefficient mostra correlações negativas, sendo potencialmente discriminativo
- **Distribuições adequadas:** Maioria das features com distribuição próxima à normal

### ⚖️ Preparação Otimizada dos Dados
- **Padronização aplicada:** StandardScaler garantiu equalização das escalas (média=0, std=1)
- **Divisão estratificada:** 70% treino (147 amostras) / 30% teste (63 amostras)
- **Proporções preservadas:** Balanceamento mantido em ambos os conjuntos (49/21 amostras por classe)
- **Prevenção de data leakage:** Scaler ajustado apenas nos dados de treino

---

## 🛠️ Metodologia Utilizada: CRISP-DM

O projeto está estruturado em torno das fases do **CRISP-DM (Cross-Industry Standard Process for Data Mining)**, garantindo uma abordagem organizada e iterativa:

1. **Business Understanding:** Definição do problema e dos objetivos de negócio.
2. **Data Understanding:** Análise exploratória para se familiarizar com o dataset.
3. **Data Preparation:** Limpeza, transformação e preparação dos dados para a modelagem.
4. **Modeling:** Implementação e comparação de diferentes algoritmos de classificação.
5. **Evaluation:** Avaliação do desempenho dos modelos e otimização de hiperparâmetros.
6. **Deployment:** Interpretação dos resultados finais e extração de insights para o negócio.

---

## 📊 Dataset

Utilizamos o **"Seeds Dataset"**, disponível publicamente no [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/236/seeds).

### Características do Dataset:

- **Total de amostras:** 210 grãos de trigo
- **Número de features:** 7 medidas geométricas
- **Classes:** 3 variedades (Kama, Rosa, Canadian)
- **Balanceamento:** Perfeito (70 amostras por classe)
- **Qualidade:** Sem valores ausentes

### Atributos Geométricos Analisados:

- Área
- Perímetro  
- Compacidade
- Comprimento do Núcleo
- Largura do Núcleo
- Coeficiente de Assimetria
- Comprimento do Sulco do Núcleo

A variável alvo é a **variedade** do trigo, com 3 classes distintas.

## 📈 Resultados da Análise Exploratória

### 🎯 Distribuições das Características:

- **area e perimeter:** Distribuições normais com leve assimetria, algumas amostras com valores elevados
- **compactness:** Distribuição concentrada (0.85-0.90), poucos outliers
- **kernel_length:** Distribuição normal com boa dispersão, sem outliers significativos  
- **kernel_width:** Distribuição uniforme com múltiplos picos, alguns outliers
- **asymmetry_coefficient:** Maior dispersão com assimetria à direita, outliers superiores
- **groove_length:** Distribuição bimodal interessante, dois picos distintos

### 🔗 Análise de Correlações:

**Correlações Muito Fortes (r > 0.95):**
- area ↔ perimeter (r = 0.99)
- area ↔ kernel_length (r = 0.95)  
- perimeter ↔ kernel_length (r = 0.97)
- area ↔ kernel_width (r = 0.97)

**Insights Importantes:**
- Características geométricas são altamente correlacionadas (esperado)
- asymmetry_coefficient apresenta correlações negativas com outras variáveis
- Excelente separação visual entre as 3 variedades no pairplot
- Dataset demonstra alta separabilidade para classificação

## 🚀 Preparação dos Dados - Status Otimizado

### ✅ Verificações de Qualidade:
- **Integridade:** 0 valores ausentes confirmados
- **Balanceamento:** 33.3% para cada classe (ideal)
- **Dimensionalidade:** Proporção 30:1 (amostras:features) favorável

### 🔄 Pré-processamento Aplicado:

1. **Mapeamento de Alvos:** Conversão de códigos numéricos para nomes descritivos
2. **Separação X/y:** Features (210×7) e target (210×1) adequadamente isolados  
3. **Padronização:** StandardScaler aplicado (média=0, desvio=1)
4. **Divisão Estratificada:** 70% treino / 30% teste com proporções preservadas

### 📊 Resultados da Divisão:

**Conjunto de Treino (147 amostras):**
- Canadian: 49 amostras
- Kama: 49 amostras  
- Rosa: 49 amostras

**Conjunto de Teste (63 amostras):**
- Canadian: 21 amostras
- Kama: 21 amostras
- Rosa: 21 amostras

---

## 🚀 Como Executar o Projeto

Para executar o notebook e replicar os resultados, siga os passos abaixo.

### 1. Clone o Repositório

```bash
git clone https://github.com/SEU-USUARIO/wheat-grain-classification.git
cd wheat-grain-classification
```

### 2. Crie e Ative um Ambiente Virtual (Recomendado)

```bash
python -m venv venv
source venv/bin/activate  # No Windows, use: venv\Scripts\activate
```

### 3. Instale as Dependências

As bibliotecas necessárias estão listadas no arquivo requirements.txt.

```bash
pip install -r requirements.txt
```

**Nota:** Se o arquivo requirements.txt não existir, você pode instalar as bibliotecas manualmente:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyterlab
```

### 4. Execute o Jupyter Notebook

```bash
jupyter lab grain_classification.ipynb
```

Após abrir o notebook, você pode executar todas as células para ver o processo de análise, treinamento e avaliação dos modelos.

---

## � Próximos Passos e Expectativas

### 🎯 Modelagem (Próxima Fase)

Com os dados preparados de forma otimizada, esperamos excelentes resultados na fase de modelagem:

- **Alta performance esperada:** Dataset com separabilidade excepcional sugere acurácia > 95%
- **Algoritmos recomendados:** SVM, KNN, Random Forest e Gradient Boosting
- **Características importantes:** Combinação de medidas geométricas será decisiva
- **Validação robusta:** Conjunto de teste estratificado garantirá avaliação confiável

### 📊 Entregáveis Finais

O projeto culminará na entrega de:

- Modelo de classificação otimizado com alta acurácia
- Comparação detalhada de performance entre algoritmos
- Identificação das características mais importantes para classificação
- Interpretação clara dos resultados e aplicabilidade prática
- Recomendações para implementação em cooperativas agrícolas

### 🔍 Insights de Negócio

- **Automatização eficiente:** Substituição do processo manual por solução baseada em dados
- **Redução de erros:** Classificação objetiva baseada em medidas precisas
- **Escalabilidade:** Solução aplicável a grandes volumes de grãos
- **Custo-benefício:** Implementação de baixo custo com alto retorno

---

## 📈 Status do Projeto

✅ **Fase 1 - Compreensão dos Dados:** Completa  
✅ **Fase 2 - Preparação dos Dados:** Completa  
🔄 **Fase 3 - Modelagem:** Em desenvolvimento  
⏳ **Fase 4 - Avaliação:** Pendente  
⏳ **Fase 5 - Implementação:** Pendente

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.8+**
- **Pandas:** Manipulação e análise de dados
- **NumPy:** Computação numérica
- **Matplotlib/Seaborn:** Visualização de dados
- **Scikit-learn:** Machine learning e pré-processamento
- **Jupyter Lab:** Ambiente de desenvolvimento interativo

---

## 📝 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

---

## 👥 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

---

**Desenvolvido com 💚 para otimizar a classificação de grãos de trigo através de Machine Learning**