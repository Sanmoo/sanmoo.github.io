---
title: "Design de API Primeiro"
date: 2025-05-01
description: "Principais ideias e insights que extraí de principles of "Web API Design: Delivering Value with APIs and Microservices"
tags: ["api-first", "api-design", "ddd"]
categories: ["apis"]
draft: true
---

Principais ideias:

* O design de um Produto de API não é uma tarefa trivial. É diferente de quando você está desenvolvendo uma API que você mesmo ou o seu próprio time irá consumir. Se você conhece os padrões de especificação de APIs tais como OpenAPI e AsyncAPI, poderá pensar desavisadamente que isso é tão simples como elaborar essas especificações e obter aprovação para o desenvolvimento. Contudo, você se depara com os alguns problemas tais como problemas:
  1. Como eu sei que minha API está resolvendo os problemas da minha empresa?
  2. Como eu sei que minha API resolverá os problemas dos meus consumidores? Quando uma API não resolve de fato os problemas que ela foi feita para resolver, é provável que caia em desuso e seu projeto fracasse.
  3. Como identificar os recursos que compõem a(s) API(s) e como identificar os limites entre elas? Quando utilizar uma ou várias APIs diferentes, por exemplo?
  4. Infelizmente é muito comum descobrir tarde demais algum ponto da API que não atende da melhor forma os consumidores, portanto falhas na sua API. Tendo isso em vista, como posso mitigar a possiblidade de retrabalho durante todo o fluxo de entrega da API, já que isso impacta bastante o tempo de entrega, é algo que queremos evitar o máximo possível, certo?
  5. Como paralelizar o trabalho com os times consumidores, para que a solução como um tudo para o problema da empresa possa ser desenvolvida o mais rápido possivel, eliminando ao máximo qualquer possível overhead de comunicação intra-times?
  
Atualmente trabalho em um time responsável por projetar e desenvoler APIs altamente estratégicas para a nossa organização. Além disso, a empresa tem passado por algumas transformações e almejado certos objetivos que tornam críticas necessidades como a eliminação de desperdício de recursos e velocidade de entrega (que se você parar pra pensar, são questões de produtividade importantes a qualquer empresa, a qualquer momento), então essas perguntas se tornaram essenciais pra mim. 

Minha empresa também tem passado por uma jornada de adesão ao DDD, Domain Driven Design, então tive que aprender e rever conceitos de DDD muito rapidamente. O Livro "Aprenda Domain-driven Design: Alinhando Arquitetura de Software e Estratégia de Negócios", que deverá ganhar um post aqui em algum momento, foi fundamental na minha jornada de aprendizado em DDD, é um livro fantástico, extremamente didático. O autor desse livro recomendou um livro sobre design de APIs, que é o livro que está na descrição desse post. Vi nesse livro a oportunidade de achar respostas para as minhas perguntas e receios.

E de fato, as achei. A ideia central do livro é expor um processo bem estruturado de Design de APIs, orientado à resolução concreta dos problemas da organização, e casa muito bem com uma abordagem DDD. Então, respondendo as perguntas acima, no formato de insights, aqui vai:

# Insight 1: Alinhe as necessidades de negócio com todas as partes interessadas - negócio, times consumidores, clientes etc., e registre os casos de uso em um formato que foca nos problemas do cliente, e não necessariamente nos atores envolvidos, como as **Estórias de Trabalho**. Cada estória de trabalho revela uma "Digital Capability" que o negócio precisa que você construa.

Esse é o começo de tudo. A partir daí você irá capturar cada **atividade** e **passos de atividade** que compõem cada uma das *digital capabilities*. Às vezes uma capability não é tão complexa ao ponto de ser composta por várias atividades e passos de atividade, mas às vezes a decomposição se torna fundamental para o entendimento de complexidades à primeira vista ocultas.

# Insight 2: A partir do que foi levantado anteriormente, encadeie a construção de uma sequência incremental de artefatos que possibilitarão, de modo estruturado e apoiado por feedback das partes interessadas, a identificação das diferentes APIs que você precisará criar, das operações que suas APIs precisarão suportar, dos recursos expostos por essas APIs e a taxonomia entre eles, e todos os detalhes das interfaces públicas dessas APIs.

O segundo insight descreve uma sequência de passos que você pode e deve realizar antes de chegar na especificação de suas APIs.

Acho que foge do escopo desse post abordar e resumir todos os pontos. O nome desse processo é ADDR (acronimo para Align, Defin, Design and Refine). Você pode obter um resumo de cada etapa no website: (https://addrprocess.com/), mas realmente recomendo a leitura caso você planeja aplicar o processo em breve.

O autor ressalta que é possível entregar APIs sem seguir um processo estruturado. Somos Engenheiros de Software, nós damos conta do recado. Mesmo que isso custe longas horas extras que se acumulam principalmente na reta final dos projetos.


a seguinte sequência de passos (e observe que cada passo do processo se apoia nos anteriores, daí a importância de fazer todos): a) Identifica limites entre APIs Distintas; b) Levante um Modelo de Perfil para Cada API, contendo todas as operações que se espera construir; c) Identifique os Recursos e a taxonomia entre eles; d) Identifique para cada operação do perfil, 



Caso de 

# Insight 2: Alinhe as necessidades de negócio com os stakeholders

Isso é uma tarefa que é atribuída geralmente ao Gestor do Produto, mas a participação de todo o time de desenvolvimento é fundamental.