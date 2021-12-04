# Guia para Caracterização de Linguagens de Programação

+ Linguagem de Programação: **Goland ou GO**

  + [Apresentação e Histórico](#apresentação-e-histórico)
  + [Características da Linguagem](#características-da-linguagem)
  + [Capacidades da Linguagem](#capacidades-da-linguagem)
  + [Produtividade do Desenvolvedor](#produtividade-do-desenvolvedor)
  + [Ecossistema](#ecossistema)
  + [Informações Adicionais](#informações-adicionais)
  + [Referências](#referências)


## Apresentação e histórico

Go é uma linguagem de programação Open Source que facilita a construção de software simples, confiável e eficiente que permite escrever um código onde performance é o foco aliada da simplicidade no desenvolvimento..
Desenvolvida no Google após frustrações com a complexidade enfrentada em outras linguagens com as quais desenvolviam seus servidores web.<br>
Robert Griesemer, Rob Pike e Ken Thompson  em 2007 grandes nome do google na responsáveis  por projetos conhecidos JavaScript V8 e sistema UNIX se reuniram para desenvolver uma linguagem que se fundamentasse três necessidades básicas do Google: desempenho, escalabilidade e facilidade de manutenção e assim nasceu o Golang ou simplesmente GOlançada pela Google em novembro de 2009.<br>
O Golang é distribuído sob licença estilo BSD.

##### Árvore genealógica do Ruby:


## Características da Linguagem
+ **Paradigma**
  : GO essencialmente é do paradigma imperativo. É modular, possui encapsulamento e polimorfismo. Embora possa embarcar outro tipo em uma estrutura que está se criando não há mecanismo de herança, opque limita o polimorfismo. Ela evita recursos que a torne multiparadigma. Ela prefere os mecanismos mais básicos.

+ **Propósito**
  : Go é linguagem que se fundamentada em três necessidades básicas do Google: desempenho, escalabilidade e facilidade de manutenção como foi explanadona na apresentação.Go possui um propósito geral, é compilada, concorrente, com garbage-collected, com tipagem forte e estática. Um dos principais pontos fortes da linguagem é sua abordagem em relação a concorrência e ao paralelismo, baseado no trabalho Communicating Sequential Processes de Filipini.

+ **Ambiente de Execução**
 : Atualmente, há dois compiladores para Go. 6g e ferramentas complementares - conhecidos em conjunto como gc - são escritos em C, usando yacc e bison para análise sintática. Além do gc, há o gccgo, um compilador de Go com front-end C++ (utilizando um analisador sintático descendente recursivo) associado ao back-end padrão do GCC.
  
+ **Implementação**
 : Go é uma linguagem compilada. Isto significa que ele converte um programa e todas as suas dependências em uma linguagem de máquina do computador.
 O comando run executa nosso código inicial, como se segue:
  ~~~
    /code
    $ go run hello.go
    /code
  ~~~
 + Ele deve exibir a seguinte linha
  ~~~
    /code

    $ Hello World

    /code
   ~~~

 + Go manipula Unicode nativamente e isto facilita o processamento de textos em qualquer idioma. Para criar um resultado de programa compilado, basta executar ir construir:
    ~~~
    /code

    $ go build hello.go

    /code
    ~~~

 + Isto gerará um arquivo executável binário, chamado hello, que pode ser executado a qualquer momento sem nenhum processo adicional.
  
+ **Custos**
  : Como o código do golang é compilado diretamente em código binário compatível com c/c ++, deve ter um desempenho interessante se comparado com linaguegens como scla que é compilado no código de byte da JVM(Java Virtual Machine).

## Capacidades da Linguagem
+ **Metaprogramação**
  : Go não suporta todos os gêneros de metaprogramação, como por exemplo não oferece suporte a macros, mas oferece suporte à reflexão em tempo de execução por meio de introspecção usando o reflect pacote.<br>
  Reflexão é a capacidade de um programa de introspectar e analisar sua estrutura durante o tempo de execução. Na linguagem Go, a reflexão é realizada principalmente com tipos. O pacote reflet oferece todas as APIs / métodos necessários para essa finalidade. 

+ **Gerenciamento de Ciclo de Vida**
  : Golang possui os seguintes escopos de variáveis:
   + Global: São as variáveis declaradas fora de qualquer bloco ou função e são acessíveis em todo o pacote onde foram declaradas. O tempo de vida dessas variáveis se encerra quando o programa se encerra.
   + Local: São variáveis declaradas dentro de uma função ou bloco de código e são vistas somente na função/bloco em que foram declaradas. O tempo de vida dessas variáveis se encerra quando a função/bloco se encerra.<br>
   **Obs**: O escopo static não existe em GO.

+ **Segurança**
  : Como Go é uma linguagem de tipo estático, há menos probabilidades de erro. Essa é uma vantagem sobre as linguagens tipadas dinamicamente com um grande número de tipos de variáveis ​​e maiores chances de erros de codificação complexos. Além disso, o código escrito em Go é mais simples e fácil de depurar. A combinação desses fatores reduz as vulnerabilidades de segurança do aplicativo.

+ **Escalabilidade**
  : Golang no quesito escalabilidade,  possui um sistema de concorrência incrível fazendo que diversos processos rode simultâneos que são os goroutines e channels.<br>
  Sem dúvida, ao lidar com projetos grandes e escaláveis, Go é uma otima opção porque ele vem com um suporte inerente para a simultaneidade descrita no paragrafo acima.

+ **Confiabilidade**
  : Golang realiza a checagem de tipos em tempo de compilação, assim diminui o risco de bugs enquanto executa o código, pois apesar de não haver necessidade de declaração, é uma linguagem fortemente tipada. É uma linguagem que permite a utilização de ponteiros e também possui funções com o intuito de dar segurança ao código, ou seja, de haver muitos bugs em aplicações complexas, como por exemplo em sistemas de segurança. Assim, temos a função Defer que atrasa a execução de uma função até que seja retornada; há o Panic que interrompe o fluxo e entra em pânico caso ocorra divergências.

+ **Concorrência e Threading**
  : Um dos pontos mais relevantes e importantes na linguagem Go é o trabalho com concorrência, Go inovou ao quebrar o modelo tradicional de threads e sua forma de utilização ao criar um novo modelo, as goroutines.  
  As goroutines são responsáveis por realizar execuções em Go de forma assíncrona. São muito poderosas e uma simples máquina de 1G de Ram e 1CPU poderá subir milhares de goroutines.<br>
  As Goroutines contribuem para tornar a simultaneidade fácil de usar. 

## Produtividade do Desenvolvedor
+ **Frameworks e Contâiners**
  + **gin**
   : O framework gin está no topo da lista em termos de popularidade devido à sua estrutura minimalista e desempenho.

  + **beego**
   : o framework beego é usada para o rápido desenvolvimento de APIs REST, aplicativos da web e serviços de back-end em Golang.

  + **eco**
   : O framework eco é outra estrutura da web de alto desempenho, extensível e minimalista em Golang.

  + **kit**
   : O framework kit é um kit de ferramentas de programação para a construção de microsserviços robustos, confiáveis e de fácil manutenção no Golang.

  + **fasthttp**
    : O framework fasthttp fornece um servidor HTTP rápido e uma API cliente que foi feita como uma alternativa ao net / http devido aos seus limites nas oportunidades de otimização.

+ **Ferramentas Disponíveis**  
  + **gofmt** : Para realização da formatação do código-fonte uniforme e automaticamente.

+ **Sintaxe, Semântica e Operações Predefinidas**
  + **Estruturas condicionais:**
          : Em Go, utilexiste o if e switch para realizar operações condicionais.
          <br> **if**
          ~~~
            if condicao: {
            # trecho codigo
            }
          ~~~
          <br>**if else**
            ~~~
              if condicao {
                # trecho codigo
              } else if condicao {
                # trecho codigo
              } else {
                # trecho codigo
              }
            ~~~
          <br> **switch**
            ~~~
              switch {
              case condicao:
                # trecho codigo
              case condicao:
                # trecho codigo
              default:
                # trecho codigo
              }
            ~~~
  + **Estruturas repetição:**
    : Go possui uma estrutura de repetição: o for. Contudo o for é flexível o suficiente para ser usado em qualquer situação que antes pedia um while ou muito raramente um do-while.
      
     <br> **for** tradicional
      ~~~
        for inicio; condicao; faca {
        #trecho codigo
        }   
      ~~~
     <br> **for** tradicional que conta com inicialização, condição e execução pós-iteração:
      ~~~
        for i:=0; i < 10; i++{
            fmt.Println(i)
        }
      ~~~
     <br> **for** como while 
      ~~~
        for len(name) < 5 {
              #trecho codigo
        }
      ~~~
     <br> **for** como foreach
      ~~~
        for index, value := range vogals {
            #trecho codigo
        }
      ~~~

## Ecossistema

+ Maturidade
  : Go passa por desenvolvimentos e aprimoramentos, no entanto, estes seguem um padrão sistemático. Golang atingiu um maior grau de maturidade devido a esse tipo de abordagem.

+ Comunidade
  : A comuniadade GO é desenvolvida e bastante acessivel. Contem varios forum e grupos de discursoes assim como encontros de desenvoveldores para discutir o futuro da linguaguem.<br>
  O Golang é distribuído sob licença estilo BSD e grande parte do desenvolvimento da linguagem se dá por ela ser totalmente open source o que quer dizer que a comunidade pode contribuir livremente para a sua melhoria.

+ Governança
  : Não foi visualidado politicas de governanças admnistradas.

+ Fragmentação
  : GO não posasui até hoje framentação da linguagem,


## Referências
+ https://go.dev/
+ https://www.geeksforgeeks.org/top-5-golang-frameworks-in-2020/
+ https://blog.betrybe.com/linguagem-de-programacao/linguagem-go-guia-completo/
+ https://jobu.com.br/2020/08/30/data-science/golang-ou-python/#O_fator_de_escalabilidade
+ https://pt.wikipedia.org/wiki/Go_(linguagem_de_programa%C3%A7%C3%A3o)
+ https://blog.cedrotech.com/golang-no-back-end
+ https://coodesh.com/blog/candidates/carreiras/go-lang-developers/
+ https://www.dinamize.com.br/blog/o-que-e-a-linguagem-de-programacao-golang-e-porque-utilizamos/
+ https://www.devmedia.com.br/primeiros-passos-com-a-linguagem-google-go/34344
+ https://digitalinnovation.one/artigos/golang-definicoes

##### Aluna: Kênia Arruda Guimrães