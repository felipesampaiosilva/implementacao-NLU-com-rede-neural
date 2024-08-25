# implementacao-NLU-com-rede-neural

Este projeto implementa um modelo de classificação de intenções utilizando um dataset de perguntas e intenções fornecido. O modelo foi desenvolvido usando o TensorFlow e Keras para criar uma rede neural com uma camada de embedding, e os resultados foram avaliados com métricas como Recall, F1-Score e um relatório de classificação.

## Estrutura do Projeto

1. **Preprocessamento dos Dados**:
   - **Tokenização e Padding**: As perguntas foram tokenizadas e transformadas em sequências numéricas. Em seguida, essas sequências foram padronizadas para um comprimento fixo usando padding.
   - **Codificação dos Rótulos**: As intenções foram codificadas em valores numéricos para serem usadas no treinamento do modelo.

2. **Modelo de Rede Neural**:
   - **Arquitetura**:
     - Uma camada de embedding com 16 dimensões.
     - Uma camada de `GlobalAveragePooling1D` para capturar a média das features.
     - Duas camadas densas com 32 e 16 neurônios, respectivamente, ativadas com ReLU.
     - Uma camada de saída com ativação softmax para classificação multi-classe.
   - **Treinamento**:
     - O modelo foi treinado por 10 épocas com um batch size de 8, usando `sparse_categorical_crossentropy` como função de perda e `adam` como otimizador.

3. **Avaliação do Modelo**:
   - **Métricas de Avaliação**:
     - Recall: `{{RECALL_RESULT}}`
     - F1-Score: `{{F1_SCORE_RESULT}}`
   - **Relatório de Classificação**:
     ```plaintext
     {{CLASSIFICATION_REPORT}}
     ```

4. **Desempenho do Modelo**:
   - **Acurácia no Conjunto de Teste**:
     - Loss: `{{LOSS_RESULT}}`
     - Accuracy: `{{ACCURACY_RESULT}}`

## Resultados Obtidos

- **Recall**: O modelo atingiu um recall de `{{RECALL_RESULT}}` no conjunto de teste, indicando uma boa capacidade de identificar corretamente as classes positivas.
- **F1-Score**: O F1-Score foi de `{{F1_SCORE_RESULT}}`, refletindo o equilíbrio entre precisão e recall.
- **Relatório de Classificação**:
  ```plaintext
  {{CLASSIFICATION_REPORT}}
