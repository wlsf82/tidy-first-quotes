# tidy-first-quotes

Algumas das minhas citações favoritas do livro [Tidy First?](https://a.co/d/ft1jGhB), de Kent Beck.

___


## Prefácio por Larry Constantine

> "Acoplamento e coesão são simplesmente medidas da complexidade do código de computador, não da perspectiva do computador que executa o programa, mas da de seres humanos tentando entender o código. Para entender qualquer programa, seja para criá-lo, corrigi-lo ou alterá-lo, é necessário entender o trecho de código imediatamente à sua frente, bem como os outros trechos aos quais ele está conectado, dos quais depende, afeta ou é afetado. É mais fácil entender o trecho de código imediato se tudo estiver interligado, se fizer sentido como um todo, se formar o que os psicólogos cognitivos chamam de gestalt. Isso é coesão. Também é mais fácil entender em termos de seus relacionamentos com outros trechos de código se esses relacionamentos forem poucos e relativamente fracos ou altamente restritos. Isso é acoplamento. Acoplamento e coesão têm tudo a ver com como seu cérebro lida com sistemas complicados."

## Introdução

> "Não estou interessado em aceleração de curto prazo. O design de software cria valor, e quando cria valor, isso se concretiza ao longo do tempo.
'Arrumar primeiro' (_tidy first_) é uma exceção. Quando você arruma primeiro, sabe que perceberá o valor da arrumação imediatamente."

## Parte I - Arrumações (_Tidyings_)

### Capítulo 5 - Ordem de leitura

> "Nenhuma ordenação de elementos é perfeita. Às vezes, você quer entender os primitivos primeiro e depois entender como eles se compõem. Às vezes, você quer entender a API primeiro e depois os detalhes da implementação. Você é o leitor, então use seu julgamento e experiência (recente). Que ordem você gostaria de ter encontrado? Dê essa sequência de presente para o próximo leitor."

### Capítulo 6 - Ordem de coesão

> "Você lê o código e descobre que, para fazer uma mudança de comportamento, precisará alterar vários pontos bastante dispersos no código e fica irritado. O que você deve fazer?
>
> Reordene o código para que os elementos que você precisa alterar fiquem adjacentes. A ordem de coesão funciona para rotinas em um arquivo: se duas rotinas estiverem acopladas, coloque-as uma ao lado da outra. Também funciona para arquivos em diretórios: se dois arquivos estiverem acoplados, coloque-os no mesmo diretório. Funciona até mesmo entre repositórios: coloque o código acoplado no mesmo repositório antes de alterá-lo.
>
> Por que não simplesmente eliminar o acoplamento? Se você sabe como fazer isso, vá em frente. Essa é a melhor organização de todas, assumindo: custo(desacoplamento) + custo(mudança) < custo(acoplamento) + custo(mudança)"

### Capítulo 11 - Declarações em pedaços (_Chunk Statements_)

> "Este ganha o prêmio de organização (_tidy_) mais simples. Você está lendo um grande pedaço de código e percebe: "Ah, esta parte faz isso e aquela parte faz aquilo". Coloque uma linha em branco entre as partes."

### Capítulo 13 - Uma pilha (_One pile_)

> "Às vezes, você lê um código que foi dividido em vários pedaços minúsculos, mas de uma forma que dificulta sua compreensão. Incorpore (_inline_) o quanto for necessário até que tudo esteja em uma grande pilha. Organize (_tidy_) a partir daí."

### Capítulo 15 - Delete comentários redundantes

> "Quando você vir um comentário que diz exatamente o que o código diz, remova-o."

## Parte II - Gerenciando (_Managing_)

> "O título deste livro é 'Arrumar Primeiro?' (_Tidy First?_), com ênfase no ponto de interrogação. Eu queria reconhecer que só porque você consegue arrumar (_tidy_) não significa que você deva arrumar (_tidy_)."

### Capítulo 16 - Arrumação separada (_Separate Tidying_)

> "Quando você se sentir confortável com a arrumação (_tidying_), trabalhando em pequenas etapas e com segurança absoluta, recomendo que você experimente não exigir avaliações para os PRs de arrumação (_tidying_)."

### Capítulo 17 - Encadeamento

> "Como a mudança é o custo dominante do desenvolvimento de software e a compreensão do código é o custo dominante da mudança, comunicar a estrutura e a intenção do código funcional é uma das habilidades mais valiosas que você pode exercitar. Comentários são uma forma de comunicação, mas a organização (_tidying_) permite explorar os limites da comunicação por meio dos outros elementos da programação."

### Capítulo 18 - Tamanhos do lote

> "Arrumar (_Tidying_) não é olhar para um futuro distante. Arrumar (_Tidying_) atende a uma necessidade imediata."

> "Quanto mais arrumações (_tidyings_) por lote, mais propensos estamos a arrumar (_tidy_) só porque sim."

> Gráfico: "Os custos de revisão aumentam à medida que os lotes diminuem"

> "Em equipes com confiança e uma cultura forte, a organização (_tidyings_) não exige revisão. O risco de interações foi reduzido a tal ponto que a organização (_tidying_) não revisada não desestabiliza o software.
> Alcançar o nível de segurança e confiança necessário para eliminar as revisões de organização (_tidying_) é um trabalho de meses. Pratiquem. Experimentem. Revisem os erros juntos."

### Capítulo 19 - Ritmo

> "O design de software tem uma tendência de 'pavimentar o caminho'."

> "Segundo Pareto, 80% das alterações ocorrerão em 20% dos arquivos."

> "Mesmo que no início você organize (_tidy_) bastante, logo você vai querer fazer uma mudança de comportamento em um código que já está organizado (_tidy_). Continue por um tempo, e a maioria das mudanças acontecerá em áreas já organizadas (_tidy_) do código. Eventualmente, encontrar código desorganizado (_untidy_) será a exceção, mesmo que a maior parte do código no sistema não tenha sido alterada."

### Capítulo 20 - Desembaraçar-se (_Getting Untangled_)

> "você não está apenas instruindo um computador, você está explicando suas intenções para o computador para outras pessoas."

### Capítulo 21 - Primeiro, depois, mais tarde, nunca (_First, After, Later, Never_)

Resumo:

> "Não arrume (_tidy_) nunca quando:
>
> - Você nunca mais vai mudar este código.
> - Não há nada a aprender melhorando o design.
>
> Arrume (_Tidy_) mais tarde quando:
>
> - Você tem uma grande quantidade de arrumação (_tidying_) para fazer sem retorno imediato.
> - Há um retorno eventual por completar a arrumação (_tidying_).
> - Você pode arrumar (_tidy_) em pequenos lotes.
>
> Arrume (_Tidy_) depois quando:
>
> - Esperar até a próxima vez para arrumar primeiro será mais caro.
> - Você não terá a sensação de estar completando se não arrumar depois.
>
> Arrume (_Tidy_) primeiro quando:
>
> - O retorno será imediato, seja na melhoria da compreensão ou em mudanças de comportamento mais baratas.
> - Você sabe o que arrumar e como."

## Parte III - Teoria

> "Compreender a teoria otimiza a aplicação"

### Capítulo 22 - Elementos Relacionados Beneficamente

> "Design de software: relacionando elementos de forma benéfica."

### Capítulo 23 - Estrutura e comportamento

TBD.

...

