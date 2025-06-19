# Exercício de Código e Questões - Redes Neurais Convolucionais

## Alunos
- Pedro Lucas Reis de Oliveira Sousa
- Pedro Amando Gandos Citelli

## Modificações Realizadas

### 1. Batch Size
- **Alteração:** De 64 para 32
- **Justificativa:** Reduzir o batch size pode melhorar a generalização do modelo, permitindo atualizações mais frequentes dos pesos e evitando overfitting.

### 2. Learning Rate
- **Alteração:** De 0.001 para 0.0001
- **Justificativa:** Learning rate menor permite treinamento mais estável e convergência mais suave, reduzindo a chance de oscilações durante o treinamento.

### 3. Paciência do Early Stopping
- **Alteração:** De 3 para 5 épocas
- **Justificativa:** Maior paciência permite que o modelo tenha mais tempo para encontrar melhorias antes de parar o treinamento, evitando parada prematura.

## Respostas às Questões

### 1. Quantas camadas convolucionais existem no modelo? Quais são seus tamanhos de kernel?

**Resposta:** Existem 2 camadas convolucionais no modelo:
- **Conv1:** kernel_size=3x3 (1 canal de entrada → 32 canais de saída)
- **Conv2:** kernel_size=3x3 (32 canais de entrada → 64 canais de saída)

### 2. Por que usamos padding nas camadas convolucionais neste código?

**Resposta:** O padding é usado para manter as dimensões espaciais da imagem após a convolução. Com padding=1 e kernel 3x3, a imagem mantém suas dimensões originais (28x28 → 28x28), preservando informações das bordas e evitando redução prematura do tamanho da feature map.

### 3. Qual a função da camada MaxPool2d? Como ela afeta as dimensões da imagem?

**Resposta:** A camada MaxPool2d reduz as dimensões espaciais da imagem selecionando o valor máximo em cada janela 2x2. Ela diminui pela metade as dimensões (28x28 → 14x14 → 7x7), reduzindo a complexidade computacional e criando representações mais robustas às pequenas variações na posição das features.

### 4. Por que precisamos "achatar" (flatten) os dados antes da camada fully connected?

**Resposta:** As camadas fully connected (Linear) esperam dados em formato 1D (vetor), mas as camadas convolucionais produzem dados em formato 3D (batch_size, canais, altura, largura). O flatten converte o tensor 3D (64, 7, 7) em um vetor 1D de 3136 elementos (64×7×7), permitindo a conexão com as camadas fully connected.

### 5. Qual a finalidade das camadas de Dropout?

**Resposta:** As camadas de Dropout previnem overfitting desabilitando aleatoriamente uma fração dos neurônios durante o treinamento. Isso força a rede a não depender excessivamente de neurônios específicos, criando uma rede mais robusta e generalizável. No modelo, Dropout2d(0.25) e Dropout(0.5) são aplicados após as camadas convolucionais e fully connected, respectivamente.

