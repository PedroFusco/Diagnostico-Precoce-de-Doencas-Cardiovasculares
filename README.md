# Diagnostico-Precoce-de-Doencas-Cardiovasculares
Neste trabalho utilizamos algoritmos de classificação para criar um modelo de diagnóstico para doença cardiovascular. O trabalho foi realizado em python.

----------------------------------------||------------------------------------------

A Empresa Cardio Catch Diseases ( CCD )
( O contexto a seguir é completamente fictício, a empresa, o contexto, o CEO, as perguntas de negócio existem somente na minha imaginação. )

A Cadio Catch Diseases é uma empresa especializada em detecção de doenças cardíacas em estágios iniciais. O seu modelo de negócio é do tipo Serviço, ou seja, a empresa ofereço o diagnóstico precoce de uma doença cardiovascular por um certo preço.

Atualmente, o diagnóstico de uma doença cardiovascular é feita manualmente por uma equipe de especialistas. A precisão atual do diagnóstico varia entre 55% e 65%, devido a complexidade do diagnóstico e também da fadiga da equipe que se revezam em turnos para minimizar os riscos. O custo de cada diagnóstico, incluindo os aparelhos e a folha de pagamento dos analistas, gira em torno de R$ 1.000,00.

O preço do diagnóstico, pago pelo cliente, varia de acordo com a precisão conseguida pelo time de especialistas, o cliente paga R$500,00 a cada 5% de acurácia acima de 50%. Por exemplo, para uma precisão de 55%, o diagnóstico custa R$500,00 para o cliente, para uma precisão de 60%, o valor é de R$ 1000,00 e assim por diante. Se a precisão do diagnóstico for 50% o cliente não paga por ele.

Observe que a variação da precisão dada pelo time de especialistas, faz com que a empresa tenha ora uma operação com lucro, receita maior que o custo, ora uma operação com prejuízo, receita menor que o custo. Essa instabilidade do diagnóstico faz com que a empresa tenha um Cashflow imprevisível.

Objetivo: criar uma ferramenta que aumente a precisão do diagnóstico e que essa precisão seja estável para todos os diagnósticos.

Neste trabalho a base de dados recebida, apesar de parecer ter alguns valores distantes da realidade, optamos por deixar o modelo de classificação dar conta disso. Para preparar os dados para a classificação os colocamos em categorias. Consideramos as faixas de risco, indicadas na literatura especializada, de colesterol, glicose, pressão arterial sistólica e diastólica e índice de massa corporal. Para a idade criamos uma faixa etária que parecia lógica.
Com as variáveis categorizadas observamos a relação de cada uma delas com a presença, ou ausência, de doença cardiovascular. Para isso visemos o uso de visualização gráfica, pois, como as variáveis não eram quantitativas, não queríamos ser enganados por uma matriz de correlação.
Tendo em mãos as variáveis que mais afetam a presença de doença cardiovascular testamos três algoritmos de classificação: DecisionTreeClassifier, Random Forest Classifier e ExtraTreesClassifier. Escolhemos o classificador Random Forest Classifier que obteve uma média de acurácia de 72.98% com intervalo de erro de [71.56%, 74.40%].
Logo, o lucro que a Cardio Catch Diseases passará a ter é de, no mínimo, R$ 2000,00.
