---
title: 🚧 Aula 01 - O que é um Programa?
---
> Nós estamos prestes a estudar a ideia de um _processo computacional_. Processos computacionais são seres abstratos que habitam computadores. À medida que se desenvolvem, processos manipulam outras coisas abstratas chamadas _dados_. A realização de um processo é dirigida por um padrão de regras chamado de _programa_. Pessoas criam programas para dirigir processos. Na prática, nós (programadores e programadoras) invocamos os espíritos do computador com nossos feitiços.
\- Structure and Interpretation of Computer Programs - Harold Abelson and Gerald Jay Sussman with Julie Sussman

Eu amo a forma como os autores do livro Estrutura e Interpretação de Programas Computacionais descrevem processos como espíritos, nos comparando a magos e magas que criam feitiços que conjuram estes espíritos para realizar tarefas.

Este é um bom ponto de partida. Se você alguma vez já tiver jogado RPG (como Dungeons and Dragons), você consegue de alguma forma se identificar com isto: A personagem é uma maga que aprende novos spells (feitiços) que manipulam a _trama_ pra que ela faça algo sobrenatural acontecer em seu favor.

Programas são como estes feitiços. Eles manipulam processos computacionais, para que eles façam algo acontecer.

Pelo menos, é melhor do que uma definição formal:
>Um programa é um conjunto de instruções que um processo computacional segue para executar uma ou mais tarefas.

_Processos computacionais_ são um conceito ligado à arquitetura de Sistemas Operacionais. Um Sistema Operacional é um tipo muito específico de programa (ou conjunto de programas) responsável por gerenciar os recursos de um computador: Memória, Disco, Processador, Placa de vídeo, comunicação com a rede, etc.

Os mais conhecidos sistemas operacionais são o Windows e o Linux, no mundo dos computadores, e Android e iOS no mundo dos dispositivos móveis (celulares smartphones, tablets, etc). Mas existem muitos outros.

Dentre as coisas que os sistemas operacionais gerenciam, se encontram a ideia de _Processos Computacionais_. Sempre que um programa qualquer precisa ser executado, o que o Sistema Operacional faz é criar um novo processo e atribuir a ele a tarefa de executar as instruções contidas neste programa, intermediando junto ao Sistema Operacional para alocar recursos (memória, processamento, disco, rede, etc). Quando todas as instruções foram devidamente executadas, ou alguma situação inesperada de falha acontece, levando-o ao estado de erro, a execução do programa é encerrada e o processo deixa de existir.

O sistema operacional faz isso o tempo todo. Se você usa Windows, você pode ser capaz de ver uma lista dos processos em execução pressionando junto as teclas _Ctrl+Shift+Escape_. Na aba _Processos_ você consegue ter uma ideia, mesmo que você não esteja fazendo nada além de assistir um vídeo, você certamente irá notar que a lista de processos em execução é extensa, e que o seu computador está mais ocupado do que você poderia imaginar. E cada um destes processos está executando um programa.

O motivo de haver tantos processos, mesmo que você esteja executando poucos programas, ilustra a grande variedade de tipos de programas que podem ser executados por um computador.

Aplicações simples como uma calculadora, um editor de textos, ou um tocador de músicas, ou mais complexas como um aplicativo de mensagens, um navegador da web, uma planilha de cálculos ou um jogo eletrônico, são os tipos mais comuns de programas que nós usamos no dia-a-dia.

Mas, ao trabalhar com programação, você irá encontrar tipos bem mais específicos de programas, como sistemas, que gerenciam recursos complexos e estabelecem uma interface para interagir com eles, e utilitários, que são ferramentas específicas para lidar com o uso destes recursos, como gerenciadores de arquivos, formatadores de discos, anti-vírus e gerenciadores de senhas e criptografia, etc.

Alguns destes programas são executados a partir da própria intervenção do usuário, como quando você abre o seu navegador para usar suas redes sociais, ou um app no celular para enviar uma mensagem. Outros programas rodam silenciosamente na memória, para disponibilizar serviços que são utilizados por outros meios, como Bluetooth, por exemplo.

E ainda existem programas com os quais você interage que sequer estão sendo executados no computador ou dispositivo móvel que você está usando. Como quando você acessa a internet. O navegador, ou o aplicativo de rede social que você usa, ambos estão sendo executados em processos no seu dispositivo, mas estão interagindo com programas remotos, que estão sendo executados em computadores ao redor do mundo, que fornecem as informações para que estes programas funcionem da forma como você espera.

Criar programas não é uma tarefa trivial. Não é como simplesmente dizer ao computador "Faça isso, faça aquilo". Há uma imaterialidade envolvida no processo que torna a atividade de criar programas análoga a algo sobrenatural. Conjurar espíritos que habitam os computadores para manipular dados usando _feitiços_ criados através de símbolos arcanos chamados linguagens de programação, é a forma mais bacana de descrever o que fazem as pessoas que criam programas.

De certa forma, você está embarcando na jornada de um "aprendiz de feitceiro", e vai aprender a conjurar estes processos e fazê-los realizar tarefas, obter dados e manipulá-los, afetando o mundo em que vivemos.

> Um processo computacional, em um computador que funciona corretamente, executa programas de forma precisa e acurada. Por isto, como aprendizes de feiticeiro, pessoas novatas em programação precisam aprender a entender e antecipar as consequências de sua conjuração. Mesmo pequenos erros (normalmente chamados de bugs ou glitches) podem ter consequências complexas e imprevizíveis.

É isto que você vai aprender neste curso: criar programas, entender e antecipar como eles deveriam se comportar, identificar e corrigir erros, e garantir que eles realizarão tarefas complexas.

## Referências
- [Building Abstraction with Procedures](https://mitp-content-server.mit.edu/books/content/sectbyfn/books_pres_0/6515/sicp.zip/full-text/book/book-Z-H-9.html#%_chap_1)
- 