# Artificial Intelligence Fundamentals
O desafio proposto é solucionar o problena da Sabor Express, uma pequena empresa de delivery de alimentos que vem enfrentando dificuldades para gerenciar suas entregas durante horários de pico, especialmente em períodos de alta demanda, como hora do almoço e jantar. Frequentemente, os entregadores demoram mais que o previsto, percorrendo rotas ineficientes, o que gera atrasos, aumento no custo de combustível e, consequentemente, insatisfação dos clientes.

Este projeto propõe uma solução baseada em Inteligência Artificial, utilizando algoritmos de busca e agrupamento para auxiliar na organização das entregas.

# Objetivo

Desenvolver uma solução capaz de:

Representar a cidade como um grafo;
Encontrar caminhos eficientes entre os pontos de entrega;
Organizar várias entregas em uma rota;
Agrupar entregas próximas em regiões;
Visualizar os resultados por meio de gráficos.

# Tecnologias e algoritmos utilizados 

O projeto foi desenvolvido com código no google colab com a linguagem em Python, utilizando:

NumPy para trabalhar com coordenadas;
Matplotlib para gerar as visualizações;
Scikit-learn para aplicar o K-Means;
A* para busca de caminhos;
K-Means para agrupamento das entregas.

As tecnologias foram escolhidas por serem simples, adequadas ao problema e fáceis de integrar. Python foi utilizado por facilitar a implementação dos algoritmos. O A* foi escolhido para encontrar caminhos eficientes no grafo, enquanto o K-Means foi utilizado para agrupar entregas próximas. O NumPy auxilia no tratamento das coordenadas, o Scikit-learn fornece o K-Means e o Matplotlib permite visualizar a rota e os agrupamentos.

# Representação da estrutura do projeto

A cidade foi representada como um grafo.
Os pontos representam locais da região de atendimento, como:

Restaurante;
Centro;
Mercado;
Escola;
Hospital;
Shopping;
Bairro A;
Bairro B;
Bairro C.

As conexões representam as ruas e seus valores representam a distância estimada em quilômetros.

# Algoritmo A*

O algoritmo A* foi utilizado para encontrar caminhos eficientes entre os pontos.
Ele utiliza o custo do caminho já percorrido e uma função heurística que estima a distância restante até o destino.

A heurística utilizada neste projeto é baseada na distância euclidiana entre os pontos.
Para organizar várias entregas, o sistema verifica as entregas disponíveis e escolhe em cada etapa, aquela que apresenta o menor custo encontrado pelo A*.

# Entregas utilizadas

Foram consideradas cinco entregas:

Entrega;
Centro;
Mercado;
Escola;
Bairro B;
Bairro C.

O ponto inicial da rota é o Restaurante.

# Agrupamento com K-Means

O K-Means foi utilizado para agrupar as entregas em regiões próximas.
Neste projeto foram definidos 2 grupos, permitindo demonstrar como pedidos próximos podem ser organizados em zonas de atendimento.

O resultado obtido foi:

-Entrega	Região
-Centro	Região 1
-Mercado	Região 1
-Escola	Região 1

-Bairro B	Região 2
-Bairro C	Região 2

# Resultados

A rota calculada pelo algoritmo foi:

Restaurante → Centro → Mercado → Centro → Escola → Bairro A → Bairro B → Bairro C

A distância total estimada pela solução foi de:
14,0 km

O projeto também gera dois gráficos:

Mapa da cidade com a rota encontrada pelo A*;

Agrupamento das entregas utilizando K-Means.


# Benefícios da solução

A proposta pode auxiliar a empresa a:

organizar melhor as entregas;
identificar caminhos eficientes;
reduzir deslocamentos desnecessários;
separar pedidos em regiões próximas;
facilitar o planejamento dos entregadores.


O projeto utiliza um mapa simulado, com coordenadas e distâncias definidas para fins acadêmicos.
Além disso, a solução não considera fatores reais como:

trânsito em tempo real;
acidentes;
bloqueios de ruas;
velocidade dos veículos;
capacidade dos entregadores;
horários específicos de entrega.

Portanto, os resultados servem como uma demonstração dos algoritmos de Inteligência Artificial aplicados ao problema de roteamento.

# Possíveis melhorias

Como evolução do projeto, seria possível:

utilizar mapas reais da cidade;
considerar trânsito em tempo real;
utilizar tempo estimado em vez de apenas distância;
permitir diferentes quantidades de entregadores;
adicionar horários e prioridades dos pedidos;
comparar diferentes algoritmos de busca;
utilizar técnicas mais avançadas de otimização.

# Como executar

O projeto pode ser executado no Google Colab.

Instalação das bibliotecas
!pip install numpy matplotlib scikit-learn

Depois, as células do notebook devem ser executadas na ordem apresentada.

https://colab.research.google.com/drive/1Fjr4olBPxfOyM_cAWCRsCVdtBzQ7HmlH?usp=sharing

# Conclusão 
Este projeto demonstra como conceitos de Inteligência Artificial, grafos, busca heurística e clustering podem ser aplicados a um problema real de logística. Aprendi que o uso do A* permite encontrar caminhos eficientes entre os pontos, enquanto o K-Means permite agrupar entregas próximas, contribuindo para uma organização mais eficiente das regiões de atendimento.
A solução apresenta, de forma prática, como algoritmos de IA podem apoiar decisões e melhorar processos de entrega.
