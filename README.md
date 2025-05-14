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
> Por que não simplesmente eliminar o acoplamento? Se você sabe como fazer isso, vá em frente. Essa é a melhor organização de todas, assumindo: `custo(desacoplamento) + custo(mudança) < custo(acoplamento) + custo(mudança)`"

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

> "Uma leitura da expressão "elementos que se relacionam beneficamente" começa com "o design é...". O que é o design? São os elementos, seus relacionamentos e os benefícios derivados desses relacionamentos.
>
> Outra leitura começa com "designers são...". O que os designers fazem? Eles relacionam elementos beneficamente."

### Capítulo 23 - Estrutura e comportamento

> "O software cria valor de duas maneiras:
>
> - O que ele faz hoje
> - A possibilidade de novas coisas que que ele possa fazer amanhã"

> "As opções são a mágica econômica do software - especialmente a opção de expansão."

> "Quanto mais volátil for o ambiente, mais valiosas as opções se tornam."

> "Comece entendendo que mudanças estruturais e comportamentais são formas de criar valor, mas são fundamentalmente diferentes. Como? Em uma palavra, reversibilidade."

### Capítulo 24 - Economia: Valor Temporal e Opcionalidade

> "O que faz sentido para nós, programadores, pode ir contra a natureza do dinheiro. Quando os imperativos nerds entram em conflito com os imperativos financeiros, o dinheiro vence. Eventualmente.
>
> Depois que minhas lições sobre a natureza do dinheiro foram absorvidas pela minha intuição, percebi que minha atitude em relação à programação estava mudando. Estratégias que faziam todo o sentido para mim agora pareciam bizarras quando contradiziam a natureza do dinheiro. Estratégias que pareciam marginais, superficiais ou ingênuas tornaram-se apenas uma gestão financeira sensata. Quanto mais eu remava com a Corrente do Comércio, mais rápido meu barco ia.
>
> A natureza que aprendi consistia em duas propriedades surpreendentes:
>
> - Um dólar hoje vale mais do que um dólar amanhã, então ganhe mais cedo e gaste mais tarde.
> - Em uma situação caótica, opções são melhores do que coisas, então crie opções diante da incerteza.
>
> Às vezes, essas duas estratégias entram em conflito. Ganhar dinheiro pode reduzir opções futuras. Mas talvez, se você não ganhar dinheiro agora, não esteja por perto para exercer essas opções futuras."

> "O design de software precisa conciliar os imperativos de 'ganhar mais cedo/gastar mais tarde' e 'criar opções, não coisas'."

### Capítulo 26 - Opções

> "O design de software é uma preparação para mudanças; mudanças de comportamento. ... O design que fazemos hoje é o prêmio que pagamos pelas "opções" de "comprar" a mudança de comportamento amanhã."

### Capítulo 27 - Opções versus fluxos de caixa

> "Arrume primeiro (_Tidy First_), com certeza. Quando:
>
> `custo(arrumação - tidy) + custo(mudança de comportamento após a arrumação - tidy) < custo(mudança de comportamento sem arrumação - tidy)`
>
> Então, arrume primeiro, com certeza.
>
> As situações mais tensas ocorrem quando:
>
> `custo(arrumação - tidy) + custo(mudança de comportamento após a arrumação - tidy) > custo(mudança de comportamento sem arrumação - tidy)`"

### Capítulo 28 - Mudanças estruturais reversíveis

> "Qual é a diferença entre um corte de cabelo ruim e uma tatuagem ruim? O corte de cabelo ruim cresce, mas a tatuagem ruim é para sempre (bem, não para sempre, mas é muito mais difícil de desfazer)."

### Capítulo 29 - Acoplamento

> "Para se prepararem para escrever seu texto clássico, _Structured Design_, Ed Yourdon e Larry Constantine examinaram programas para descobrir o que os tornava tão caros. Eles notaram que todos os programas caros tinham uma propriedade em comum: mudar um elemento exigia mudar outros elementos. Os programas baratos tendiam a exigir mudanças localizadas."

#### Cascata

> "Mudanças em cascata são o maior problema.
>
> Você usará o design de software para reduzir a probabilidade e a magnitude das mudanças em cascata."

> "Quando dizemos que um sistema é "complexo", queremos dizer que as mudanças têm consequências inesperadas."

> "O que o acoplamento significa para responder à pergunta "Devo arrumar primeiro?". Às vezes, quando você está começando uma mudança complicada, é o acoplamento que está te incomodando: "Mas se eu mudar isso, terei que mudar tudo isso também". Bagunça. Reserve um minuto para analisar a lista de arrumações e ver qual delas reduziria o acoplamento.
> 
> O acoplamento aumenta o custo do software."

### Capítulo 30 - Equivalência de Constantine

> "O objetivo do design de software é minimizar o custo do software (e também maximizar o valor)."

> "Quanto mais cedo recebermos feedback do uso real, menos tempo/dinheiro/oportunidade gastaremos em comportamentos que não importam."

> "O custo do software é aproximadamente igual ao custo de alterá-lo.
>
> `custo(software) ~= custo(mudança)`

> O custo da mudança é aproximadamente igual ao custo das grandes mudanças:
>
> `custo(mudança) ~= custo(grande mudança)`
>
> O que torna essas mudanças caras tão caras? É que mudar este elemento requer mudar aqueles dois elementos, cada um dos quais requer mudar outros elementos, e... e... O que "propaga" as mudanças? Acoplamento. Portanto, o custo do software é aproximadamente igual ao acoplamento:
> 
> `custo(grande mudança) ~= acoplamento`
>
> E agora temos a Equivalência de Constantine completa:
> 
> `custo(software) ~= custo(mudança) ~= custo(grande mudança) ~= acoplamento`
>
> Ou para destacar a importância do design de software:
> 
> `custo(software) ~= acoplamento`
> 
> Para reduzir o custo do software, precisamos reduzir o acoplamento."

### Capítulo 31 - Acoplamento versus desacoplamento

> "Aqui está algo em que acredito, mas não consigo provar ou explicar adequadamente: quanto mais você reduz o acoplamento para uma classe de mudanças, maior se torna o acoplamento para outras classes de mudanças. A implicação prática disso (se corresponder à sua intuição) é que você não deve se preocupar em extrair até a última gota de acoplamento. O acoplamento criado ao fazer isso não vale a pena."

> "Design de softwere é dífícil - _software design is hard._"

### Capítulo 32 - Coesão

> "Não faça mudanças bruscas. Você está trabalhando com informações incompletas e variáveis ​​sobre o que está associado ao quê. Não reorganize tudo drasticamente. Mova um elemento de cada vez. Deixe o código mais organizado (_tidier_) para a próxima pessoa. Se todos seguirem a regra do escoteiro ("deixe melhor do que encontrou"), o código se tornará mais prático com o tempo."

### Capítulo 33 - Conclusão

> "E com isso você está preparado(a) para responder à pergunta "arrumar primeiro?" repetidamente. Cada vez de forma ligeiramente diferente, mas sempre afetado pelas mesmas forças:
>
> - Custo - A arrumação (_tidying_) tornará os custos menores, mais tarde ou menos prováveis?
> - Receita - A arrumação (_tidying_) tornará a receita maior, mais cedo ou mais provável?
> - Acoplamento - A arrumação (_tidying_) fará com que eu precise alterar menos elementos?
> - Coesão - A arrumação (_tidying_) fará com que os elementos que preciso alterar estejam em um escopo menor e mais concentrado?
>
> O mais importante, porém, é você. A arrumação (_tidying_) trará paz, satisfação e alegria à sua programação? Talvez um pouco. Isso é importante porque, se você for a sua melhor versão, será um/uma programador(a) melhor. Você não pode ser a sua melhor versão se estiver sempre com pressa, se estiver sempre alterando código que é doloroso de alterar."

> "Arrumações (_tidyings_) são os _Pringles_ do design de software. Quando estiver arrumando (_tidying_) primeiro, resista à vontade de comer o próximo. Arrume (_tidy_) para permitir as próximas mudanças de comportamento. Guarde a maratona de arrumação (_tidying_) para depois, quando você pode pirar sem atrasar a mudança que outra pessoa está esperando."

> "Arrumar primeiro? (_Tidy First?_) Provavelmente sim. Só o suficiente. Você merece."
