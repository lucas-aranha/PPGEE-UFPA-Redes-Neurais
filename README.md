# AVALIAÇÃO III - BACKPROPAGATION       

## DESCRIÇÃO
Este repositório contém o desenvolvimento do trabalho avaliativo nº3 da disciplina de Redes Neurais Artificiais (PPGEE0219), do Programa de Pós-Graduação em Engenharia Elétrica (PPGEE-UFPA). Ele consiste na implementação de uma rede Perceptron de Múltiplas Camadas (MLP) do zero, sem o uso de bibliotecas específicas de Machine Learning (ML). O algoritmo
BackPropagation padrão deveria ser implementado em qualquer linguagem de programação,
sem auxílio de funções já definidas para implementar qualquer função da rede neural. O
critério de parada é feito pela validação cruzada, há possibilidade de variar o número de
neurônios na camada escondida e funções de ativação para os neurônios, bem como verificar
valores dos pesos sinápticos antes e após finalização do treinamento.

## DOCUMENTAÇÃO

**`NeuralNetwork`:** classe Python que possui dez funções distintas. São elas:    

### 1 INICIALIZAÇÃO
1.1 `__init__(self, input_size, hidden_size, output_size, activation)`: Esta função é
chamada ao criar uma instância da classe NeuralNetwork. Ela inicializa a rede neural com o
tamanho de entrada especificado, tamanho da camada oculta, tamanho de saída e função de
ativação.     

**Parâmetros:**     
`input_size`: o número de features de entrada.     
`hidden_size`: o número de neurônios na camada oculta.        
`output_size`: o número de neurônios de saída.             
`activation`: a função de ativação a ser usada pelos neurônios.       

### 2 FUNÇÕES DE ATIVAÇÃO
2.1 `activation_func(self, x)`: Esta função aplica a função de ativação à entrada x e retorna
o resultado. Ela suporta as seguintes funções de ativação: sigmoid, ReLU, tanh e linear.   

2.2 `activation_func_deriv(self, x)`: Esta função calcula a derivada da função de ativação
em relação a x. Ela é usada durante o processo de retropropagação para calcular os
gradientes.    

### 3 FORWARD PASS       
3.1 `forward_pass(self, X)`: Esta função executa a passagem para frente da rede neural
dada a entrada X. Ela calcula a soma ponderada das entradas na camada oculta, aplica a
função de ativação e, em seguida, calcula a soma ponderada e a ativação da camada de saída.        

**Parâmetros:**       
`X`: os dados de entrada.

### 4 BACKWARD PASS      
4.1 `backward_pass(self, X, y, hidden_output, output_output, learning_rate)`: Esta
função executa a passagem para trás da rede neural, atualizando os pesos com base nos erros
e gradientes calculados.    

**Parâmetros:**      
`X`: os dados de entrada.      
`y`: a saída de destino.           
`hidden_output`: a saída da camada oculta.        
`output_output`: a saída da camada de saída.        
`learning_rate`: a taxa de aprendizado usada para atualizações de peso.

### 5 TREINAMENTO DA REDE    
5.1 `train(self, X, y, epochs, learning_rate, early_stopping=False, patience=5,
validation_data=None)`: Esta função treina a rede neural nos dados de treinamento
fornecidos X e y.   

**Parâmetros:**      
`X`: os dados de treinamento de entrada.     
`y`: os dados de treinamento de saída.       
`epochs`: o número de épocas de treinamento.        
`learning_rate`: a taxa de aprendizado usada para atualizações de peso.   

### 6 INSPEÇÃO DE PESO SINÁPTICO     
6.1 `get_weights(self)`: Esta função retorna os pesos atuais da rede neural.        
6.2 `print_weights(self)`: Esta função imprime os pesos atuais da rede neural.

### 7 FUNÇÃO DE PREVISÃO        
7.1 `predict(self, X)`: A função de previsão é responsável por fazer previsões nos dados de
entrada. Dada uma matriz de entrada X, a função calcula a passagem direta através da rede
neural para gerar previsões.     

**Parâmetros:**      
`X`: os dados de entrada.

### 8 FUNÇÃO DE ACURÁCIA      
8.1 `calculate_accuracy(self, X, y)`: é usada para avaliar a precisão das previsões da rede
neural em um determinado conjunto de dados. Ele compara as saídas previstas com os rótulos
verdadeiros e calcula a métrica de precisão.    

**Parâmetros:**     
`X`: os dados de entrada.     
`y`: os dados de saída

