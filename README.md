# Projeto: Agente de IA CardioPredict 4.0

### 1. Identificação do Grupo
* **Instituição:** Fundação Salvador Arena
* **Curso:** Engenharia de Controle e Automação
* **Grupo:** Grupo X
* **Integrantes:**
    * Diego Marques de Carvalho - RA: 21002603

---

### 2. Área Problema Selecionada
Selecione a trilha tecnológica do projeto (marque com um [x]):
* [X] **Saúde 4.0:** Robótica Assistiva (Controladores Inteligentes/Fuzzy)
* [ ] **Smart Grid:** Eficiência Energética e Descarbonização
* [ ] **Agtech:** Automação de Precisão e Visão Computacional
* [ ] **Logística Autônoma:** Coordenação de AGVs e Otimização de Rotas

---

### 3. Diagnóstico e Definição do Agente
Nesta seção, descrevemos o cenário de atuação e a modelagem do agente inteligente.

* **Contexto:** O projeto aplica-se ao setor de saúde digital e monitoramento intensivo, onde a velocidade de diagnóstico é o fator determinante entre a vida e a morte em eventos cardiovasculares.
* **Problema:** A dificuldade de identificar padrões sutis em sinais vitais que precedem um infarto, resultando em diagnósticos tardios em ambientes de triagem ou monitoramento remoto.
* **Impacto:** A implementação deste agente visa reduzir o tempo de resposta médica e aumentar a precisão na identificação de pacientes de alto risco, reduzindo a taxa de mortalidade hospitalar.

#### Modelagem PEAS (Agente Inteligente)
| Componente | Descrição |
| :--- | :--- |
| **Performance (P)** | Minimizar falsos negativos; Alcançar acurácia superior a 85% na classificação de risco. |
| **Ambiente (E)** | Sistema de monitoramento de UTI ou dispositivo vestível (wearable) de telemedicina. |
| **Atuadores (A)** | Painel de alerta para a equipe de enfermagem; Disparo de notificação de emergência. |
| **Sensores (S)** | Leitura de pressão arterial, frequência cardíaca, idade, nível de colesterol e ECG. |

---

### 4. Arquitetura de Dados e IA
Definição das fontes de dados e da inteligência por trás da solução.

* **Origem dos Dados:** [Heart Attack Dataset - Kaggle](https://www.kaggle.com/datasets/fatemehmohammadinia/heart-attack-dataset-tarik-a-rashid).
* **Lógica de IA:** Redes Neurais Artificiais (Multilayer Perceptron).
* **Justificativa:** Redes neurais são altamente eficientes no processamento de grandes volumes de dados tabulares médicos, permitindo encontrar correlações não lineares entre os sintomas e o desfecho clínico do paciente.

---

### 5. Plano de Tratamento de Dados (ETL)
O fluxo de processamento dos dados segue estas etapas:
1. **Extração:** Leitura automatizada do arquivo `heart_attack_dataset.csv` via biblioteca Pandas.
2. **Transformação:** Normalização de dados numéricos (Min-Max Scaling), tratamento de valores ausentes (Imputação pela média) e codificação de variáveis binárias.
3. **Carga:** Armazenamento dos tensores prontos para o modelo na pasta `/data/processed`.

---

### 6. Estrutura do Repositório
Organização simplificada para o Milestone 1:
* `/data`: Arquivos de dados originais (raw) e tratados (processed).
* `/notebooks`: Experimentos iniciais de análise exploratória e correlação.
* `/scripts`: Códigos Python (.py) contendo a classe do Agente e scripts de ETL.
* `requirements.txt`: Lista de bibliotecas (Numpy, Pandas, Scikit-learn, TensorFlow).
* `README.md`: Documentação técnica do projeto.

---

### 7. Instruções para Execução
Para reproduzir o ambiente e testar o diagnóstico:
1. Clone este repositório.
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
