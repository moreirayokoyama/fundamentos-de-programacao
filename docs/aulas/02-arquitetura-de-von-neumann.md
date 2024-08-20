---
title: 🚧 Aula 02 - Arquitetura de Von Neumann
---
Responder como um programa funciona é uma questão que demanda certo nível de abstração. É sempre possível se aprofundar em mais camadas de detalhe da resposta. E, quanto mais detalhes a gente tentar cobrir, mais e mais a gente se afasta do que realmente seja importante para os propósitos deste curso. Ainda assim, à medida que você se especializar cada vez mais em programação, mais relevante estes detalhes se tornarão.

Mas aqui a gente vai tentar não se aprofundar mais do que o suficiente para dar uma resposta concreta à pergunta "o que eles fazem?", e tentar provocar em você alguma curiosidade para se aprofundar mais no futuro.

## O que é a Arquitetura de Von Neumann
Em 1945, John von Newmann definiu os elementos primários de um computador com propósito de cálculos genéricos, e ele descreveu o sistema em cinco subdivisões:
Controle Central, Memória Principal, Meio de Entrada, Meio de Saída, e Mídia de Gravação. O Controle Central (que hoje chamamos de CPU, ou Unidade Central de Processamento) seria, por sua vez, formada por cinco outros subsistemas: a Unidade de Controle, um Oscilador de Clock (que é basicamente um sincronizador), a Unidade Lógica e Aritmética (ULA, ou ALU em inglês), uma memória interna para Registradores, e um cache para a memória.

Esta arquitetura se replica nos múltiplos núcleos de um processador moderno, embora existam diferentes designs entre os fabricantes de processador, e eu não pretendo entrar em detalhes a respeito destas diferenças neste curso, até por que eu não domino esta área.

O importante aqui é entender como a CPU funciona:
- Processadores possuem um ciclo de trabalho, que se repete indefinidamente desde o momento em que ele é ligado até o momento em que a energia é cortada, o ciclo de trabalho do processador é: 
	- Fetch: buscar da memória a próxima instrução a ser executada
	- Decode: decodificar a instrução para entender o que precisa ser feito
	- Execute: Executar a instrução
	- Store: armazenar o resultado da instrução
- Cada passo deste ciclo é executado sempre que o oscilador de clock emite um pulso elétrico
- O oscilador de clock funciona em uma frequência determinada pela capacidade do processador. Por exemplo, atualmente o recorde de performance em um processador é de pouco mais de 9Ghz, o que significa que o oscilador emite mais de 9 bilhões de pulsos elétricos por segundo.

Existem detalhes aqui específicos do design de processadores modernos que incluem pipelining e execução superescalar, que torna os processadores capazes de administrar mais de um ciclo de trabalho simultaneamente, tornando-os muito eficientes. Além é claro de recursos como interrupções, polling e Acesso Direto à Memória para que o processador se organize enquanto executa operações mais lentas do que a capacidade em que ele opera (como interagir com o disco ou com a rede).

Se você está achando essa explicação abstrata demais, eu realmente te encorajo a estudar Arquitetura e Organização de Computadores.

Vamos focar neste ciclo de trabalho do processador, por que é aí onde reside a execução do nosso programa. Quando iniciamos a execução de um programa, o Sistema Operacional cria um processo (como descrevemos na aula anterior), alocando uma quantidade de memória onde o programa será carregado e os dados usados durante a sua execução serão manipulados.

Quando o processo é criado, o sistema operacional inicializa o contador de programa para o endereço da sua primeira instrução. É aí que o ciclo de trabalho da CPU na arquitetura de von Neumann entra em ação. O processador realiza o fetch (busca da instrução), decodifica e executa a tarefa, e segue para a próxima instrução.

Lembrar agora da definição mais formal de programa que fizemos na aula anterior pode fazer mais sentido, então eu vou repetí-la para refrescar nossa memória:

>Um programa é um conjunto de instruções que um processo computacional segue para executar uma ou mais tarefas.

Então o processador começa da primeira instrução, executa o ciclo de trabalho fetch->decode->execute->store, vai para a próxima instrução, e repete este fluxo de novo e de novo até que chega ao término do programa, e o processo é finalizado, deixando de existir.

Não é nada tão romântico e lúdico quanto a ideia de tratar os processos como seres que conjuramos com nossos feitiços, mas agora você tem uma ideia mais concreta de como as coisas funcionam.

Mas como são estas instruções o programa possui e que o processador precisa executar?

Tudo o que uma instrução de um programa faz é instruir o computador a ler dados em uma ou mais mídias de entrada (teclado, rede, um drive de armazenamento, microfone, etc), e os registra na memória, executa alguma operação nestes dados (como operações aritméticas ou lógicas) e escreve o resultado da operação em uma ou mais mídias de saída (disco, rede, vídeo, dispositivo de som, etc).

E, embora tudo isto pareça ser simplista, é repetindo este ciclo inúmeras vezes (milhões, ou até mesmo bilhões por segundo) que torna possível ser feito tudo o que testemunhamos com a tecnologia (reprodução de filmes em alta resolução, interações com jogos 3D, navegar pela internet e assistir a conteúdo sendo transmitido por streaming, enquanto se ouve música e se usa um software para pintura digital, por exemplo).

É claro que deixamos de lado aqui uma série de detalhes sobre como os sistemas operacionais lidam com diversos programas simultaneamente, além da ação de outros componentes, como a unidade de processamento das placas de vídeo (GPUs) e outros coprocessadores, mas eu acho que para concluir a nossa ideia do que é um programa e como ele funciona, eu diria que o nosso objetivo foi cumprido. E volto a dizer: se você ficou interessado em saber mais sobre isso tudo, procure aprender sobre Arquitetura e Organização de Computadores. Existem diversos livros sobre o assunto, além de ser uma disciplina clássica em graduações de Ciência da Computação.

O que há de mais importante neste modelo arquitetural é, talvez, compreender o seguinte: É muito comum ouvirmos dizer que a CPU é o cérebro do computador. Apesar disto, a CPU não é, nem de longe, uma entidade dotada de inteligência própria. Tudo o que ela faz é exatamente o que ela é instruída a fazer. Literalmente. Nem mais, e nem menos. E é a habilidade da pessoa de entender isto, de compreender as peculiaridades deste princípio, e de ser capaz de, através desta compreensão, antecipar o comportamento do computador, junto com as particularidades da linguagem de programação que está usando (e, inerentemente, da plataforma onde ela roda), que a torna uma programadora boa ou ruim.

A partir de agora, nós iremos dedicar nosso foco para discutir como os programas são construídos.

## Referências
- [Arquitetura de Von Newmann](https://pt.wikipedia.org/wiki/Arquitetura_de_von_Neumann)
- [Essential Computer Science](https://learning.oreilly.com/library/view/essential-computer-science/9781484271070/)