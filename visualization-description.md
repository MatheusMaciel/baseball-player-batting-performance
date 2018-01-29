#Resumo

O primeiro gráfico deixa claro que a maioria dos jogadores usam a mão direita para rebater. Entretanto, nos dois gráficos seguintes é possível notar que tanto para o *batting average* quanto *home runs* os jogadores canhotos possuem melhor desempenho que os demais. Além disso, não foi possível notar relação entre características fisícas como peso e altura e o desempenho do jogador, como pode ser visto no último gráfico.

Concluindo, fica claro que se um time pretende escolher um rebatedor, escolher um jogador que rebate com a mão esquerda pode garantir um desempenho melhor.

#Design

Dado que o objetivo da visualização é comparar o desempenho dos jogaroes, fica claro que as duas principais medidas de comparação são *batting average* e *home runs*. Dessa forma, essa variáveis são codificadas nos eixos x e y, respectivamente.

Com exceção do nome do jogador, as variáveis restantes podem ser usadas para agrupar (*handedness*) ou quantificar (*weight* e *height*) os jogadores. Dado a natureza categórica de *handedness*, ela foi codificada usando cor. 

No caso de *weight* e *height*, o formato númerico faz com que a utilização de canais como distância e área boas opções de codificação.

Sendo assim, bubble chart parece ser uma escolha sólida de gráfico para apresentar 3 variáveis númericas e uma categórica. Por isso, decidi agregar as variáveis *weight* e *height* em nova variável chamada *weight/height ratio* que será codificada no raio na bolha. 

Ainda assim, é importante contextualizar o leitor então decidi criar 3 gráficos de barra que mostrarão o comportamento do jogadores agrupados pode *handedness*. O primmeiro vai mostrar a quantidade de jogadores por mão usada. O segundo vai mostrar a média de *batting average* e o terceiro a quantidade de *home runs*.

#Feedback

OBS.: Como alguns reviews foram longos, vou citar pontos importantes aqui e as versões originias estarão no zip desse projeto.

### Review 1
- Referente a versão v1 da visualização.
- Referente à revisão: reviews/review_v1-R1.txt
- De maneira geral o revisor R1 foi capaz de compreender o objetivo geral da visualização dado que várias das dúvidas levantas envolvem a adição de mais informação com o intuito de aprofundar a análise.
- A utilização da cor da bolha claramente foca a análise do revisor na mão usada para rebater.
- Certos pontos mais específicos da visualização e seu contexto mão ficaram tão claros. Para resolver esse ponto, alterei o título da visualização, o título do eixo x e adicionei uma explicação sobre o que é *Batting average* na descrição da visualização.
- Na revisão, o revisor confunde algumas legendas (trocou canhoto por ambidestro). Conversando com o mesmo sobre a revisão ele confirmou que conseguiu entender bem as legendas e que o erro foi apenas falta de atenção na escrita da revisão.

### Review 2
- Referente a versão v2 da visualização.
- Referente a revisão: reviews/review_v2-R2.txt
- Assim como a o revisor anterior, R2 conseguiu compreender o contexto e o objetivo da visualização sendo capaz de gerar perguntas mais profundas sobre a informação apresentada.
- A cor da bolha consegue focar a análise do revisor na comparação da mão usada para rebater.
- R2 também conseguiu indentifcar a barreira de desempenho do *batting average* em 0.3.
- O principal problema apontado nessa revisão foi a variável *weight/height ratio* que não ficou clara. Para resolver esse problema será adicionado uma explicação na descrição da visualização e a unidade da variável na legenda.
- A revisão também apontou que as bolhas estão sobrepondo os *tick labels*.

### Review 3
- Referente a versão v2 da visualização.
- Referente a revisão: reviews/review_v2-R3.txt
- O revisor R3 foi capaz de identificar que não existe diferença clara na mão utilizada para rebater, e que o aumento do *batting average* a quantidade de *home runs* tende a aumentar.
- Assim como os demais revisores, R3 também levantou questões com o objetivo de aprofundar a analise feita.

### Resultados
Com base nas revisões anteriores, acredito que a versão 2 da visualização consegue atingir bem seu objetivo. Entretanto, eu não estou contente com a grande quantidade de sobreposição para baixos valores de *home runs* (entre 0-50). Decidi aplicar uma escala logarítmica no eixo y (gerando a versão 3 da visualização). Após isso, conversei com os 3 revisores sobre a nova versão. 

Os revisores chegaram a conclusão que a versão 3 consegue transmitir a mesma informação transmitida pela versão 2 mas também permiti uma nova descoberta:
- A maior parte dos jogadores com *batting average* baixo e poucos *home runs* usam a mão direita para rebater.

Sendo assim, decidi escolher a versão 3 como versão final.

### Pós revisão udacity - Versão 4

Após a revisão do udacity, decidi adicionar 3 gráficos de barra para mostrar o *batting average*, *home runs* e a quantidade de jogadores por mão usada para rebater. Dessa forma, consigo dar uma visão geral do desempenho dos jogadores e o último gráfico consegue aprofundar mais a análise incluindo a alura e o peso do jogador. 

#Recursos

- http://dimplejs.org/advanced_examples_viewer.html?id=advanced_interactive_legends
- https://github.com/PMSI-AlignAlytics/dimple/wiki
- http://colorbrewer2.org/#type=qualitative&scheme=Set2&n=3
- https://bost.ocks.org/mike/bubble-map/ (legendas da area do circulo)