# MLP com MNIST - Comparação com e sem PCA

**Aluno:** Pedro Lucas Reis de Oliveira Sousa  
**Matrícula:** 202220818  
**Instituição:** UNIFOA

## Sobre

Implementação de MLPClassifier do Scikit-Learn para classificação do dataset MNIST, comparando performance com e sem redução de dimensionalidade usando PCA.

## Principais Implementações

- ✅ Normalização de dados (resolução do problema de loss alto)
- ✅ PCA com 95% de variância mantida
- ✅ Comparação de modelos com e sem PCA
- ✅ Análise de performance e visualizações
- ✅ Otimização de hiperparâmetros (Adam, early stopping)

## Resultados

- **Redução de dimensionalidade:** 80% (784 → ~154 features)
- **Performance mantida** com PCA
- **Tempo de treinamento otimizado**
- **Redução de overfitting**

## Tecnologias

- Python
- Scikit-Learn
- NumPy
- Matplotlib

## Como Executar

```bash
jupyter notebook Sklearn_MLP_com_MNIST_Incompleto.ipynb
```

Execute todas as células sequencialmente para ver os resultados completos.
