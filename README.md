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



