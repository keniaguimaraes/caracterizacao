# Atividade A1 - Go

+ **a) modelo de tradução (compilação, etc.?)**
  + Go é uma linguagem compilada. Isto significa que ele converte um programa e todas as suas dependências em uma linguagem de máquina do computador.
    O comando run executa nosso código inicial, como se segue:
    Go manipula Unicode nativamente e isto facilita o processamento de textos em qualquer idioma.

+ **b) nomes, variáveis e vinculação**
  + Go utiliza a palavra var, o nome da variável que queremos referenciar e seu tipo. 
  + Variáveis são declaradas explicitamente e usadas pelo compilador para, por exemplo, checar o tipo-correção das funções chamadas. o compilador verifica os tipos usados em dados e variáveis para garantir que sempre está sendo usado um tipo que é esperado em todas as situações.
  + A linguagem suporta vinculação dinâmica e estática.

+ **c) escopo, tempo de vida e ambientes de referência.**
  + Escopo:  delimitado por {} (chaves) - Não pode abrir chaves depois de newline. Variáveis definidas em blocos internos nãio são visíveis em blocos externos.
  + Tempo de vida: A liguagem GO possui um  O coletor de lixo. Ele se encarrega de desalocar espaço de memória não mais utilizado. O coletor de lixo tem controle sobre o tempo de vida de variáveis e estruturas.

## Referências

+ Linguagem Go: guia prático e rápido sobre Golang 2021
https://blog.betrybe.com/linguagem-de-programacao/linguagem-go-guia-completo/