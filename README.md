# DeverAI - Exercícios de Redes Neurais e Data Science

**Instituição:** UNIFOA
**Disciplina:** Redes Neurais e Data Science
**Aluno:** Pedro Lucas Reis de Oliveira Sousa

---

## 📚 Sobre o Repositório

Este repositório contém exercícios práticos e implementações de algoritmos de Machine Learning, Redes Neurais e técnicas de Data Science desenvolvidos durante o curso na UNIFOA. Os exercícios abordam desde conceitos fundamentais até implementações avançadas de redes neurais convolucionais.

---

## 🗂️ Estrutura do Projeto

### 📁 [Exercicio-PCA/](./Exercicio-PCA/)

Exercícios relacionados à **Análise de Componentes Principais (PCA)** e sua aplicação em Machine Learning.

#### 📂 [Comparacao/](./Exercicio-PCA/Comparacao/)

- **Arquivo:** `Sklearn_MLP_com_MNIST_Incompleto.ipynb`
- **Descrição:** Implementação completa de MLPClassifier para classificação do dataset MNIST
- **Principais Features:**
  - ✅ Comparação de performance com e sem PCA
  - ✅ Redução de dimensionalidade (784 → ~154 features)
  - ✅ Normalização de dados e otimização de hiperparâmetros
  - ✅ Análise de performance e visualizações
  - ✅ Early stopping e otimização com Adam

#### 📂 [Exercicio2/](./Exercicio-PCA/Exercicio2/)

- **Arquivo:** `California_Housing.ipynb`
- **Descrição:** Implementação completa de MLPRegressor para regressão do dataset California Housing
- **Principais Features:**
  - ✅ Comparação de performance com e sem PCA
  - ✅ Análise de variância explicada e redução dimensional
  - ✅ Visualizações comparativas e análise de resultados
  - ✅ Validação cruzada e métricas detalhadas (MAE, RMSE, R²)
  - ✅ Pipeline completo com pré-processamento e PCA

### 📁 [Redes Neurais Convolucionais/](./Redes%20Neurais%20Convolucionais/)

Implementação e análise de **Redes Neurais Convolucionais (CNN)** para classificação de imagens.

#### 📄 `2025_1_Treinamento_de_modelo_CNN_para_MNIST.ipynb`

- **Descrição:** Treinamento completo de modelo CNN para classificação MNIST
- **Colaboração:** Pedro Lucas Reis de Oliveira Sousa + Pedro Amando Gandos Citelli
- **Principais Features:**
  - ✅ Arquitetura CNN com 2 camadas convolucionais
  - ✅ Otimização de hiperparâmetros (batch size, learning rate)
  - ✅ Early stopping com paciência ajustada
  - ✅ Análise detalhada de cada componente da rede
  - ✅ Respostas teóricas sobre funcionamento das CNNs

---

## 🚀 Como Executar

### Pré-requisitos

```bash
# Instalar dependências
pip install jupyter numpy pandas matplotlib seaborn scikit-learn torch torchvision
```

### Executar Notebooks

```bash
# Para exercícios de PCA - MNIST
jupyter notebook "Exercicio-PCA/Comparacao/Sklearn_MLP_com_MNIST_Incompleto.ipynb"

# Para exercícios de PCA - California Housing
jupyter notebook "Exercicio-PCA/Exercicio2/California_Housing.ipynb"

# Para exercícios de CNN
jupyter notebook "Redes Neurais Convolucionais/2025_1_Treinamento_de_modelo_CNN_para_MNIST.ipynb"
```

---

## 📊 Principais Resultados

### MLP com PCA (MNIST)

- **Redução de dimensionalidade:** 80% (784 → ~154 features)
- **Performance mantida** com PCA
- **Tempo de treinamento otimizado**
- **Redução significativa de overfitting**

### MLP com PCA (California Housing)

- **Redução de dimensionalidade:** ~25% (8 → ~6 features)
- **Análise de variância explicada** com visualizações
- **Comparação detalhada** de métricas (MAE, RMSE, R²)
- **Validação cruzada** para robustez dos resultados

### CNN para MNIST

- **Arquitetura:** 2 camadas convolucionais + pooling + fully connected
- **Otimizações:** Batch size 32, Learning rate 0.0001
- **Early stopping:** Paciência de 5 épocas
- **Performance:** Alta acurácia com boa generalização

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- **Scikit-Learn** - MLPClassifier, MLPRegressor, PCA, métricas
- **PyTorch** - Redes Neurais Convolucionais
- **NumPy** - Manipulação de arrays
- **Pandas** - Manipulação de dados
- **Matplotlib** - Visualizações
- **Seaborn** - Visualizações estatísticas
- **Jupyter Notebook** - Ambiente de desenvolvimento

---

## 📈 Conceitos Abordados

### Machine Learning

- Redução de dimensionalidade (PCA)
- Normalização e pré-processamento
- Otimização de hiperparâmetros
- Validação cruzada e early stopping
- Classificação e regressão
- Análise de variância explicada

### Redes Neurais

- Perceptrons Multi-Camadas (MLP)
- Redes Neurais Convolucionais (CNN)
- Backpropagation
- Regularização (Dropout)

### Data Science

- Análise exploratória de dados
- Visualização de resultados
- Métricas de performance (MAE, RMSE, R²)
- Comparação de modelos
- Análise de dimensionalidade
- Pipeline de pré-processamento

---

## 📝 Estrutura dos Exercícios

Cada exercício contém:

- **Objetivo claro** e contexto teórico
- **Implementação completa** com comentários explicativos
- **Análise de resultados** e visualizações
- **Discussão teórica** dos conceitos aplicados
- **Conclusões** e insights obtidos

---

## 🎯 Próximos Passos

- [ ] Implementar mais técnicas de redução de dimensionalidade (LDA, t-SNE)
- [ ] Adicionar exercícios de redes neurais recorrentes (RNN/LSTM)
- [ ] Explorar datasets mais complexos (CIFAR-10, ImageNet)
- [ ] Implementar técnicas de transfer learning
- [ ] Adicionar exercícios de ensemble methods
- [ ] Implementar análise de feature importance

---

## 👥 Contribuidores

- **Pedro Lucas Reis de Oliveira Sousa** - *Desenvolvimento e implementação principal*
- **Pedro Amando Gandos Citelli** - *Colaboração em Redes Neurais Convolucionais*

---

## 📚 Referências

- [Scikit-Learn Documentation](https://scikit-learn.org/stable/)
- [PyTorch Documentation](https://pytorch.org/docs/)
- [MNIST Dataset](https://www.openml.org/d/554)
- [UNIFOA - Redes Neurais e Data Science](https://unifoa.edu.br/)

---

*Repositório criado para fins acadêmicos - UNIFOA 2025*
