---
layout: post
title: Análise de redes e alguns gráficos
categories: [análise de redes, visualização]
tags: [SNA, análise de redes, grafo]
comments: true
---

Fiz uma postagem em uma rede social para grupo de bolsistas, com a figura de um gráfico que estava fazendo no momento. Não fazia ideia que teria tanta repercussão! Nesta postagem vou falar um pouco sobre análise de redes e algumas formas de visualização.

<!--more-->

![Gráfico de arcos](/img/grafico_arco.png)

Esse é o gráfico que despertou o interesse do pessoal. O que ele mostra? Cada ponto é um município e os arcos representam a existência de relacionamento entre os municípios. Neste caso, com Barretos, SP, especificamente. A espessura dos arcos acompanha a intensidade do relacionamento e a cor do arco representa a UF do município.

Não irei falar agora o que são estes relacionamentos, pois ainda não publiquei este estudo ;-) Mas o conceito deste tipo de análise pode ser útil para vários tipos de análises, onde exista uma *rede*.

Em alguns fenômenos, torna-se interessante estudar não só seus elementos mas a relação entre eles. Pense em uma sala de aula, por exemplo. Podemos estudar a turma calculando médias das notas, proporções, correlações... mas ainda estaremos perdendo uma dimensão importante do ambiente escolar: os alunos se relacionam, conversam, trocam informações e etc.

Para analisar estes relacionamentos, precisamos entender o fenômeno como uma rede. Neste caso, cada aluno é um *nó* da rede e cada relacionamento entre os alunos é uma *aresta*. Se definirmos o relacionamento como "amizade", temos um relacionamento sem direção: A é amigo de B da mesma forma que B é amigo de A. Existem outros tipos de redes onde podem existir direção no relacionamento, como em "Quem passou o boato para frente?". Outras redes podem ter ponderação nestes relacionamento, por exemplo: "Quantas vezes eles conversaram esta semana?".

A análise de redes é um campo que está se expandindo rapidamente, com o advento das redes sociais, mas tem uma origem antiga, ainda na teoria dos grafos. Uma aplicação muito comum é analisar redes sociais (dessas on-line ou mesmo off-line), e vemos o termo "Análise de Redes Sociais" surgir. Mas lembre que os métodos não se limitam a redes sociais, tudo que se comporta em rede pode ser analisado por esta metodologia, fazendo adaptações quando necessário.

Na Análise de Redes, eu percebo quatro grandes áreas de pesquisa: análise de centralidade, detecção de comunidades, visualização e simulação. Vou falar sobre as três primeiras.

## Análise de centralidade

Voltando ao exemplo da sala de aula. Qual é o aluno mais popular da sala? Provavelmente aquele que tem mais amigos, ou seja, o que tem maior número de arestas. Essa quantidade de arestas que cada nó possui é chamada de *grau*. Partindo deste e outros valores, diversas medidas de centralidade foram criadas, visando medir a *proeminência* de um nó na rede.

## Detecção de comunidades

Na sala de aula é comum termos o grupinho da frente e a turma "da cozinha", por exemplo. Em geral, estes dois grupos até se relacionam um pouco, mas é de forma limitada. Existem algoritmos que consideram a centralidade dos nós e seus relacionamentos e detectam estas possíveis "comunidades".

## Visualização

Essa é a area que causa o fenômeno "Uau! Que bonito!" rsrs. As visualizações de redes tendem a ser bem coloridas e inovadoras, mas precisamos manter um pé na realidade e questionar o que elas estão informando.

![Sóciograma](https://upload.wikimedia.org/wikipedia/commons/3/39/Moreno_Sociogram_3rd_Grade.png)

A visualização mais comum é o sóciograma. Em boa parte destas visualizações, é um gráfico em duas dimensões onde os nós costumam ser dispostos no centro de acordo com a sua centralidade. Quanto maior a interação entre dois nós, mais perto eles ficam. Mas existem outras formas de construir estes sóciogramas, então certifique-se sobre qual algoritmo foi usado antes de interpretar o gráfico.

![Gráfico de arcos](https://datavizcatalogue.com/methods/images/top_images/arc_diagram.png)

Uma outra forma de visualização de redes é o gráfico de arcos. Considero ele especialmente útil para visualizar um pedaço da rede, para poder visualizar melhor algumas relações específicas entre os nós.

## Para saber mais

Livros e artigos:
  * Wasserman e Faust. [Social Network Analysis](https://books.google.com.br/books?id=CAm2DpIqRUIC&lpg=PP1&hl=pt-BR&pg=PP1#v=onepage&q&f=false)
  * Barabási. [Network science](http://networksciencebook.com)
  * Luke e Harris. [Network analysis in public health: history, methods, and applications](http://www.ncbi.nlm.nih.gov/pubmed/17222078)
  
Softwares:
  * R e pacote [igraph](http://igraph.org/r/)
  * Pacote que usei para fazer o diagrama de arco no R: [arcdiagram](https://github.com/gastonstat/arcdiagram)
  * [Gephi](http://igraph.org/r/)

Softwares que ainda não usei:
  * [UCINET](https://github.com/gastonstat/arcdiagram)
  * [Pajek](http://mrvar.fdv.uni-lj.si/pajek/)
  * [SocNetV](http://socnetv.org)