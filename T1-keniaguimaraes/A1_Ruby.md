# Atividade A1 - Ruby

+ **a) modelo de tradução (compilação, etc.?)**
  + Ruby é uma abrangentimente mencionado como linguagem compilda. A saída dessa compilação é então interpretada, pelo menos em alguns casos - também existem implementações que o JIT compila (Rubinius e IIRC JRuby compila no bytecode Java depois de um tempo). 

+ **b) nomes, variáveis e vinculação**
  + Nomes em Ruby são usados para se referir a constantes, variáveis, métodos, classes e módulos. O primeiro caractere de um nome ajuda o Ruby a distinguir o uso pretendido. 
  + Variáveis no Ruby podem conter dados de qualquer tipo. Você pode usar variáveis em seus programas Ruby sem qualquer declaração. O nome de uma variável por si só denota seu escopo (local, global, instância, etc). Variáveis de instância iniciam com @ e variáveis de classe com @@
  + Ruby faz vinculação dinâmica.
 
+ **c) escopo, tempo de vida e ambientes de referência.**
  + Ruby possui um escopo estático, ou seja, suas variáveis têm seus escopos determinados antes da execução do programa.
  + O tempo de vida de variáveis locais: ambos limitado ao método referenciado. Já ariáveis de instânciae variáveis de classes: possuem escopo local e tempo de vida estático.
  
## Referências

+ https://medium.com/@rogeriozambon/escopo-de-vari%C3%A1veis-do-ruby-cd3952c8f738
Escopo de variáveis do Ruby

+ https://guru-sp.github.io/tutorial_ruby/nomes-em-ruby.html
Tutorial de Ruby do GURU-SP
