# California Housing - MLPRegressor com PCA

**Aluno:** Pedro Lucas Reis de Oliveira Sousa  
**Matrícula:** 202220818  
**Instituição:** UNIFOA

## Sobre

Implementação de MLPRegressor do Scikit-Learn para regressão do dataset California Housing, comparando performance com e sem redução de dimensionalidade usando PCA.

## Objetivos do Exercício

### O que se espera responder:
1. **PCA melhora a performance de modelos de regressão?**
2. **Qual o impacto da redução dimensional em datasets pequenos?**
3. **Quando PCA é benéfico vs quando não é?**
4. **Como analisar variância explicada e escolher componentes?**
5. **Quais métricas usar para comparar modelos de regressão?**

## Principais Implementações

- ✅ Análise de variância explicada pelo PCA
- ✅ Comparação de MLPRegressor com e sem PCA
- ✅ Visualizações comparativas e análise de resultados
- ✅ Validação cruzada (5-fold) para robustez
- ✅ Métricas detalhadas: MAE, RMSE, R²
- ✅ Pipeline completo: Pré-processamento → PCA → MLPRegressor

## Resultados Obtidos

### Análise de Dimensionalidade
- **Features originais:** 8
- **Features após PCA:** 6 (25% de redução)
- **Variância mantida:** 95%

### Performance dos Modelos
| Modelo | MAE | RMSE | R² | CV R² (média) |
|--------|-----|------|----|--------------| 
| Baseline | 0.8740 | 1.1731 | -0.0502 | N/A |
| MLP SEM PCA | 0.3675 | 0.5428 | 0.7752 | 0.7696 |
| MLP COM PCA | 0.4609 | 0.6455 | 0.6821 | 0.6853 |

## Por que PCA NÃO melhorou aqui?

### 1. **Dataset Pequeno**
- Apenas 8 features originais
- Todas as features são relevantes para o problema
- Redução de 8→6 não é significativa o suficiente

### 2. **Features Já Otimizadas**
- California Housing tem features bem selecionadas
- Não há redundância significativa entre variáveis
- Cada feature contribui para a predição

### 3. **Overfitting Não é Problema**
- Dataset não é complexo o suficiente
- MLPRegressor com 8 features não sofre overfitting
- Regularização natural do dataset

### 4. **Perda de Informação**
- 25% de redução dimensional remove informação útil
- PCA força projeção em espaço menor
- Informação perdida é mais valiosa que ganho computacional

## Quando PCA É Benéfico?

### ✅ **PCA MELHORA quando:**
- **Muitas features** (centenas/milhares)
- **Alta correlação** entre variáveis
- **Overfitting** é problema real
- **Ruído** nas features originais
- **Computação** é limitada

### ❌ **PCA NÃO melhora quando:**
- **Poucas features** (< 20)
- **Features já selecionadas** (como este caso)
- **Baixa correlação** entre variáveis
- **Informação perdida** é valiosa

## Conclusões do Exercício

1. **PCA não é universalmente benéfico** - depende do dataset
2. **Análise de variância explicada** é crucial para decidir
3. **Métricas de regressão** (MAE, RMSE, R²) mostram impacto real
4. **Validação cruzada** confirma robustez dos resultados
5. **Visualizações** ajudam a entender o comportamento

## Tecnologias

- Python
- Scikit-Learn (MLPRegressor, PCA, métricas)
- NumPy, Pandas
- Matplotlib, Seaborn

## Como Executar

```bash
jupyter notebook California_Housing.ipynb
```

Execute todas as células sequencialmente para ver os resultados completos.

## Arquivos Gerados

- `artifacts/model_without_pca.joblib` - Modelo sem PCA
- `artifacts/model_with_pca.joblib` - Modelo com PCA  
- `artifacts/metrics_comparison.txt` - Métricas detalhadas
- `artifacts/results_comparison.csv` - Tabela comparativa
