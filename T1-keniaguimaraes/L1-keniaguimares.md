
# Guia para Caracterização de Linguagens de Programação

+ Linguagem de Programação: **Ruby**

  + [Apresentação e Histórico](#apresentação-e-histórico)
  + [Características da Linguagem](#características-da-linguagem)
  + [Capacidades da Linguagem](#capacidades-da-linguagem)
  + [Produtividade do Desenvolvedor](#produtividade-do-desenvolvedor)
  + [Ecossistema](#ecossistema)
  + [Informações Adicionais](#informações-adicionais)
  + [Referências](#referências)

## Apresentação e Histórico
Ruby é uma linguagem de programação multiparadigma, de tipagem dinâmica e forte. Desenvolvida no Japão em 1995, por Yukihiro "Matz" Matsumoto, para ser usada como linguagem de script. O Ruby é totalmente gratuita como também é livre para utilizar, copiar, modificar e distribuir.
Inicialmente, Matz estudou outras linguagens em busca de encontrar uma sintaxe ideal. Recordando a sua busca, disse, “Eu queria uma linguagem interpretada que fosse mais poderosa do que Perl e mais orientada as objetos do que Python2.”


## Características da Linguagem

+ **Paradigma**
  :Ruby é uma linguagem de programação interpretada multiparadigma, de tipagem dinâmica e forte. Suporta programação funcional, orientada a objetos, imperativa e reflexiva. Foi inspirada principalmente por Python, Perl, Smalltalk, Eiffel, Ada e Lisp, sendo muito similar em vários aspectos a Python 
  Em Ruby, tudo é um objeto. Cada parcela de informação e código podem receber as suas próprias propriedades e ações. A Programação orientada a objetos denomina as propriedades como variáveis de instância e as ações como métodos. A aproximação pura, da orientação aos objetos do Ruby, é geralmente demonstrada pelo seguinte trecho de código que aplica uma ação a um número.
  

+ **Propósito**
  : Seu criado Yukihiro “Matz” Matsumoto falou quando pensou na criação do ruby “Estou tentando tornar o Ruby natural, não simples”. Pensando na facilidade e na união  1ue equilibra a programação funcional com a programação imperativa juntou  partes das suas linguagens favoritas (Perl, Smalltalk, Eiffel, Ada e Lisp) que resultou no ruby.
   "O Ruby é simples na aparência, mas muito complexo no interior, tal como o corpo humano!". 

+ **Sistema de Tipagem**
  : Ruby é dinamicamente, implicitamente e fortemente tipada.
  + Dinamicamente tipada
     Quer dizer que a cada interação, o tipo é verificado. Isso fica claro no seguinte exemplo:
       ~~~
        x = 100
        y = 3
        x + y
       ~~~
  + Implicitamente tipada
    Em Ruby não precisamos declarar o tipo de x. Ou seja, não foi necessário fazer algo como: integer x = 100. Isso acontece pelo fato do Ruby detectar o tipo de cada variável em tempo de execução.

  + Fortemente tipada
    Todas as variáveis devem ter um tipo, ou seja, fazer parte de uma classe, no caso do Ruby, e que cada tipo segue a risca seu contrato. Por exemplo:
        ~~~
          a = 100
          b = "Ruby on Rails"
          a + b
        ~~~
  + Em ruby não podemos somar um String com INteiro.
  + Os tipos básicos em Ruby são números, strings, arrays, hashes, intervalos, símbolos e expressões regulares.

+ **Ambiente de Execução**
  : Ruby possui vários interpretadores para executar como por exemplo o MRI (“Matz’s Ruby Interpreter”, o “Interpretador de Ruby do Matz”) ou CRuby (já que é escrito em C).  O interpretador original da linguagem é o irb  que vem junto a instalação. 

+ **Implementação**
  : A implementação 1.8.7 padrão é escrita em C, como uma linguagem de programação de único passe. Não há qualquer especificação da linguagem, assim a implementação original é considerada de fato uma referência. 
  + Atualmente, há várias implementações alternativas da linguagem, incluindo YARV, JRuby, Rubinius, IronRuby, MacRuby e HotRuby, cada qual com uma abordagem diferente, com IronRuby, JRuby[ e MacRuby fornecendo compilação JIT e, JRuby e MacRuby] também fornecendo compilação AOT. A partir das séries 1.9 em diante Ruby passou a utilizar por padrão a YARV (Yet Another Ruby VirtualMachine) substituindo a Ruby MRI (Matz's Ruby Interpreter).

+ **Custos**
  :Quanto maior a complexidade e quanto mais recursos contém a linguagem, maior o grau de dificuldade de aprendizado. Ruby é uma linguagem de fácil aprendizado, diminuindo o tempo necessário para treinamento. Essa característica está ligada a sua sintaxe baseada em outras linguagens.

## Capacidades da Linguagem

+ **Metaprogramação**
  : Metaprogramação em Ruby é, na realidade, bem simples e isso se dá pelo fato de que todo código Ruby é executado, não há separação entre fases de compilação e runtime, cada linha de código é executado contra um self particular.
  Um aspecto da metaprogramação em Ruby que se destaca é ser capaz de perguntar ao nosso código questões sobre si mesmo durante o tempo de execução. Isso também é conhecido como introspecção. Assim como podemos nos fazer perguntas como “Por que estou aqui?”, nosso código pode fazer o mesmo, embora as perguntas não possam ser tão existenciais.
  Podemos perguntar a qualquer objeto se ele tem a capacidade de fornecer uma resposta a uma chamada de método específico antes de fazê-lo usando o método respond_to?.
  ~~~
      "Roberto Alomar".respond_to? :downcase
      
      # => true
      
      "Roberto Alomar".respond_to? :floor
      
      # => false
  ~~~

+ **Gerenciamento de Ciclo de Vida**
  : Ruby possui um escopo estático, ou seja, suas variáveis têm seus escopos determinados antes da execução do programa.
  + O tempo de vida de variáveis locais: ambos limitado ao método referenciado. Já ariáveis de instânciae variáveis de classes: possuem escopo local e tempo de vida estático.

+ **Segurança**
  : A linguagem tem suporte a exceções, possibilitando o tratamento de erros previstos pelo programador. Porém, ela possui suporte a aliasing, possibilitando vários nomes referenciando variáveis/objetos idênticos, causando sinonímia. Com o uso de exceções, o programa se torna seguro para problemas previstos, mas o uso de alias é prejudicial para sua confiabilidade.
  + Com estes pontos, podemos dizer que Ruby é uma linguagem segura.

+ **Performance**
  : Ruby é uma linguagem interpretada e as linguagens interpretadas tendem a ser mais lentas do que as compiladas.Ruby usa coleta de lixo o que impacta na sua perfomance.Chamadas de método Ruby são lentas (embora, por causa da digitação em pato, sejam indiscutivelmente mais rápidas do que em linguagens interpretadas fortemente tipadas)
  Ruby também leva mais tempo para processar. Comparado ao Java, Ruby é 20% mais lento no processamento.

+ **Escalabilidade**
  : Ruby on Rails é perfeito para um produto focado em escalabilidade.

+ **Confiabilidade**
  : Por sua dinamicidade, não definimos categoricamente como a variável deveria se comportar, podendo ocorrer comportamentos inesperados em tempo de execução.
  + A linguagem tem suporte a exceções, possibilitando o tratamento de erros previstos pelo programador. Porém, ela possui suporte a aliasing, possibilitando vários nomes referenciando variáveis/objetos idênticos, causando sinonímia. Com o uso de exceções, o programa se torna seguro para problemas previstos, mas o uso de alias é prejudicial para sua confiabilidade.

+ **Concorrência e Threading**
  : Ruby permite concorrrencia contudo  o compilar Mats recomensa o uso de Processes em vez de Threads para concorrência.Eles aumentam exponencialmente a complexidade da sua base de código, e essa é a principal razão pela qual a documentação recomenda.
  + Uma Thread permite que o utilizador do programa utilize determinada funcionalidade do ambiente enquanto outras Threads processão outras operações.Toda vez que você executa ruby, rails ou irb, você está criando um processo. Dentro de cada processo, você tem algo que está executando o código no seu processo. Isso é chamado de thread.
  Seu sistema operacional começa todo processo com uma thread “principal”. O Ruby permite que você crie quantas threads adicionais você desejar, chamando Thread.new com um bloco de código a ser executado. 
    ~~~
      t1 = Thread.new do
        i = 0
        1_000_000.times do
          i += 1
        end
      end

      t2 = Thread.new do
        j = 0
        1_000_000.times do
          j += 1
        end
      end
    ~~~

## Produtividade do Desenvolvedor

+ **Frameworks e Contâiners**
  + **Ruby on Rails**
  : É um framework web de backend de Ruby que foi originalmente fundado em 2004. Este é um dos frameworks Ruby mais populares, com 49 mil estrelas no GitHub. 

  + **Sinatra**
  : Alternativa gratuita e de código aberto para Ruby on Rails, então você deve considerar o Sinatra. É a biblioteca e estrutura da web de Ruby que foi lançada em 2007. Comparado com Rails, não funciona em padrões MVC. Sim, acredita na criação de aplicações web espontaneamente.

  + **Camping:**
  : Considerado um dos os melhores frameworks Ruby, deixando de fora o Camping é impossível. Sendo uma das estruturas que menos ocupam espaço, deve ter um design admiravelmente notável.

  + **Ramaze:**
  : Para estruturas que envolvem motores de modelagem, o Ramaze Ruby Framework é uma escolha a ser observada, com toda a honestidade. A complexidade com a qual o programa foi projetado para facilitar o acesso o torna o melhor na corrida.

  + **Goliath**
  : Se você está procurando um Ruby Web Framework assíncrono, sua busca termina com Goliath. A estrutura estabelece sua autoridade sobre a maioria das estruturas disponíveis no mercado com sua notável variedade de recursos.

  + **Padrino**
  : O Framework da Web de código aberto mais elegante e elegante é escrito em Ruby por aí. Padrino pode ser o Padre de todos eles. Baseado na Biblioteca Web do Sinatra, está configurado para codificar aplicativos avançados com facilidade.

  + **NYNY**
  : O NYNY, ou, literalmente, o framework New York, New York, é um dos mais incrivelmente pequenos Ruby Web Frameworks. As estruturas consistem em frameworks micro-web que são usados ​​para testar aplicativos quanto à sua compatibilidade com os navegadores de hoje.

  + **Resque:**
  : Resque é uma estrutura de trabalho em segundo plano em Ruby que foi desenvolvida pelo CEO e cofundador do GitHub, Chris Wanstrath. A estrutura apoiada por Rides é usada principalmente para criar filas para jobs em espera e, em essência, não é diferente de Jobs atrasados.


+ **Ferramentas Disponíveis**
  : Seguem algumas das principais ferramentas diponiveis para ruby.
  + **Rubygems** : Repositório de bibliotecas.
  + **Rubocop:** : Analisador de código estático Ruby
  + **Bundler:** : Bundler é uma ferramenta que garante que as **gems** de que você precisa estejam presentes no desenvolvimento, teste e produção
  + **Rake:** : Rake é uma ferramenta de gerenciamento de tarefas de software e automação

    
+ **Sintaxe, Semântica e Operações Predefinidas**
  + **Estruturas condicionais:**
    + No ruby há o **if else** demonstra no codigo abaixo:
    ~~~~
    if condicao
      # trecho de código a ser executado quando a condição for verdadeira
    end
    ~~~~
    + Exemplo de **If Else**
    ~~~~
    if condicao
      # trecho de código a ser executado quando a condição for verdadeira
    else
      # trecho de código a ser executado quando a condição for falsa
    end
    ~~~~
    + Exemplo de **elsif**
     ~~~~
        if condicao_1
          # trecho código a ser executado quando a condição_1 for verdadeira
        elsif condicao_2
          # trecho de código a ser executado quando a condição_2 for verdadeira
        elsif condicao_3
          # trecho de código a ser executado quando a condição_3 for verdadeira
        end
     ~~~~

   + Há também o  **case** queé  é uma estrutura condicional que nos permite substituir vários testes com if. 
    ~~~~
    case variavel
      when valor1
        # trecho de código 1
      when valor2
        # trecho de código 2
      else
        # trecho de código 3
    end
    ~~~~

   + **Estruturas repetição:**
    : A linguagem Ruby possui três estruturas de controle de repetição: o for, o each e o times.
      
    + O **for**  é uma estrutura de repetição muito comum.
     ~~~~
      for variavel in expressao
            # Trecho de código
      end
      ~~~~  

    + O each na verdade não é considerado não é uma estrutura de repetição, mas sim um método. Esse metodos varre um onjeto e pode ser usado como uma estrutura de repetição.
      ~~~~
      expressao.each do |variavel|
        # Trecho de código
      end
      ~~~~

    + times também não é uma estrutura de controle de repetição, mas sim um método da classe Integer. Contudo, o método times também é muito utilizado para executar trechos de código repetidamente.
    ~~~~
    expressao.times do
      # Trecho de código 
    end
    ~~~~

  + Legibilidade e Redigibilidade
    : A legibilidade na linguagem Ruby sofre influência direta da forte utilização de orientação a objetos. Como seu próprio criador comenta: "Ruby is really, really object oriented programming". O código resultante é bastante limpo (poucas linhas e poucas instruções), porém a legibilidade pode ficar prejudicada pela alta ortogonalidade da linguagem, pois há diversas formas de representar a mesma ação.

    Redigibilidade ○ Ruby possui uma maior preocupação com sua redigibilidade do que com a legibilidade
          
 
## Ecossistema

+ Maturidade
  : Ruby é considerado uma linguagem  madura pois possui uma vasta comunidade  e possui uma evolção constante que se adapta as necessidade do mercado.

+ Comunidade
  : A comunidade de ruby que cresce em torno de uma linguagem de programação é uma das suas maiores forças. O Ruby tem uma comunidade vibrante eé crescente, que se mostra juda os desenvolvedores de todos os níveis de conhecimento. O canal de IRC do Ruby éumotimo lugara para se trocar experiencias e as  Conferências de Ruby sempre acontecem juntamente com desenvolvedoras ma]is experientes discutindo o futuro da linguagem.

+ Governança
  : Ruby é uma linguaguem mandura portanto conclui-se que o possui um dos sistemas de governança mais robustos entre as linguagens de programação FOSS utilizadas na atualidade, o que sugere estabilidade e sucesso de longo prazo ao projeto.

+ Fragmentação
  : Exsitem varias implemnatcoes de ruby com a ajuda de frameworks com suporte em suas comunidades. Cabe ao desenvolvedor decidir qual variação é mais interessante.

## Referências
+ https://blog.back4app.com/pt/top-10-ruby-frameworks/
+ http://www.tutorialspoint.com/ruby/
+ https://www.ruby-lang.org/pt/documentation/ruby-from-other-languages/
+ https://lpunb.fandom.com/wiki/Semin%C3%A1rio_sobre_Ruby_-_2012/2_-_Grupo_2
+ http://mislav.uniqpath.com/poignant-guide/ - site do livro "Why's (Poignant) Guide to Ruby", uma abordagem divertida e eficiente de aprendizado da linguagem
+ https://guru-sp.github.io/tutorial_ruby/
+ https://medium.com/@rogeriozambon/escopo-de-vari%C3%A1veis-do-ruby-cd3952c8f738
+ RANGEL, E. Conhecendo Ruby. [S.l.]: Leanpub, 2014.
+ SOUZA, L. Ruby: aprenda a programar na linguagem mais divertida. 1. ed. São Paulo: Casa do Código, 2012. v. I.


##### Elaborado por Kênia Arruda Guimrães