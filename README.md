# Como funciona um computador

Para podermos entender como funciona um computador, temos que ter em mente que ele não é uma super máquina que tem consciencia própria e faz coisas sem precisar da intervenção humana, na verdade, um computador faz
tarefas simples. 

Um computador vê o mundo através de cálculos, tudo que ele executa segue um caminho específico, como numa linha de produção de uma fábrica. Se pedirmos para um computador fazer um cálculo simples, como `(3+6)/2`, ele executará vários passos para resolver essa equação, primeiro alguma parte fará a multiplicação, e o resultado será passado para uma outra parte para fazer a divisão, e assim por diante. 

![imagem input output aqui](./input-output.png)

De fato, tudo o que um computador faz é computar, como uma calculadora, sempre há um `input` (entrada) e um `output` (saída). O nosso trabalho como desenvolvedores é desenvolver os algorítimos que usam essa entrada, e trabalham com ela de alguma maneira até que tenhamos o resultado desejado como saída. 

# Sistema binário

![imagem input output aqui](./binary-numbers-texture-vector-31657194.jpg)

Para que nós possamos nos entender melhor com as máquinas que vamos programar, precisamos entender o que é ciência da computação, é claro que não vamos cobrir tudo o que envolve ciência da computação no decorrer dos 3 meses deste curso, mas iremos ter uma noção básica de como as coisas funcionam.

Como este é o primeiro capítulo do curso, a primeira coisa que podemos fazer é contar quantos alunos temos na sala, e se contarmos nos dedos podemos representar cada aluno com um dedo levantado na minha mão, claro, que não conseguimos contar uma grande quantidade de pessoas dessa maneira, mesmo que eu usasse minha duas mãos, ainda só terei dez dedos. Esse tipo de operação tem um nome específico, ela é chamada de notação unária, por que para cada dedo levantado nas minhas mãos, eu atribuo uma única unidade de valor na contagem que estou fazendo.

Esse é um sistema bem universal, que todo mundo usa no dia a dia. Mas e quando eu preciso contar valores mais altos? 

Claro que todo mundo sabe que podemos usar um sistema mais útil, que todo mundo aprendeu na escola,
o sistema decimal. 

Agora não atribuímos um valor a cada dedo levantado, mas sim, aprendemos que temos 10 digitos que podemos usar para representar qualquer número que quisermos, além do `0-9`, também conseguimos representar
o 11, 12 e assim por diante, e é por trabalhar sempre com 10 possíveis dígitos [0-9] que ele é chamado de `base 10`.

Mas os computadores não aprenderam matemática com a gente na pré-escola. Eles não usam o sistema decimal para contar alguma coisa, de fato, eles usam um sistema muito mais simples, que para a gente pode parecer mais complexo e complicado, mas no final do dia, os computadores foram desenvolvidos por humanos, e são relativamente simples.

Então, qual a linguagem que os computadores usam?

Eles usam a linguagem binária, enquanto nós usamos de 0 à 9 na `base 10` um computador usa de 0 à 1 na `base 2`.

Mas por que não usar também o sistema decimal como nós usamos normalmente? Por que as pessoas que inventaram os primeiros computadores tiveram que criar todo esse novo sistema binário que só usa dois dígitos?

Bom, o que os computadores precisam para funcionar? O que um computador aguarda antes de iniciar algum processo?  Eletricidade! A única coisa que um computador, smartphone ou qualquer pedaço de tecnologia pra funcionar é de eletricidade, a única interação física de um computador com a gente é a eletricidade.

Por exemplo, todos temos uma lâmpada no quarto, que pode estar acessa. Mas ela pode ser apagada também, só precisamos apretar um botão, um switch. 

E qual a relação dessa lâmpada, dessa ideia de que o fluxo de eletricidade pode acender ou apagar tem a ver com os computadores? 

Nós, a partir de um impulso elétrico, podemos representar uma informação. 

> Zeros e Uns.

É por isso que no final das contas, tudo que um computador usa são impulsos elétricos como `input`. Quando queremos representar o dígito `1` precisamos de energia, quando não fornecemos energia, temos um `0`.

Agora sabemos que quando a lâmpada está acessa, temos um `1` e quando ela está desligada, temos um `0`, mas e quando precisamos contar além de um dígito?

Eu poderia, claro, usar mais de uma lâmpada! Se tivessemos mais de três lampadas, quantos dígitos poderíamos representar usando o sistema binário, ou seja, somente zeros e uns?

000 = 0  
001 = 1  
010 = 2  
011 = 3  
100 = 4  
101 = 5  
110 = 6   
111 = 7  

A resposta é 7!

Percebam que seguimos um padrão, que não foi por acaso, mas que é muito fácil de entender.

## Diferenças entre o sistema decimal (base-10) e binário (base-2)

Se te mostrassem o número `123`, como você o leria? 

Claro, cento e vinte e três. Nós sabemos disso por que aprendemos no sistema decimal que em cada posição, temos um peso diferente para cara dígito, então os dígitos continuam indo somente de 0 à 9, porém assumem valores diferentes com base na posição em que se encontram.

No exemplo do `123` temos o seguinte:

![imagem input output aqui](./123.png)

A cada casa mais a esquerda multiplicamos em 10 vezes o valor da casa da direita e o resultado da multiplicação desse número pelo dígito decimal logo a baixo representa o valor que esse dígito está assumindo.

![imagem input output aqui](./10.png)

E no sistema binário temos a mesma situação, so que ao invés de usarmos a base 10, usamos a base 2.

![imagem input output aqui](./000.png)

----

Tudo o que a gente viu até agora tem a ver com lâmpadas, mas de onde vem esses zeros e uns que um computador realmente usa?

É o que está dentro do computador, não são lâmpadas, mas sim minusculos interruptores, bilhões deles, que podem estar ligados ou desligados.

# Representação de dados no sistema binário

Agora que já sabemos sobre como o computador se comunica com os nossos comandos e como ele conta, podemos pensar em não só dígitos numéricos, mas como transformar esses inputs (zeros e uns), em dados mais complexos,  como um caracter, para formar uma palavra.

#### Como podemos representar uma letra, usando somente o sisterma binário?

As pessoas que inventaram os primeiros computadores tiveram uma ideia muito simples, para cada letra do alfabeto foi atribuído um valor numérico, assim nasceu a tabela `ASCII`.

[imagem tabela ASCII]

Então para cada número, temos um caracter mapeado, não só letras, mas todos os ascentos, caracteres especiais, pontos, virgulas e etc...

> Exemplos:

````
1000001 = 65 = A  
1000010 = 66 = B  
````

Mas essa tabela, que foi inventada a muito tempo atrás e só compreendia os caracteres do idioma inglês, e não todos os caracteres, de todas as línguas do mundo, sendo assim, teve que ser criada mais uma tabela para unificar o jeito que os computadores interpretam os caracteres essa é o sistema `UNICODE`, esta reserva um valor muito maior de espaço para acomodar todos os caracteres possíveis, bem como novos que ainda possam surgir.

Um exemplo de caractere que não existia na primeira tabela `ASCII` e foi criado posteriormente e suportado pelo sistema de `UNICODE`: 😂

#### Já sabemos como representar dígitos e textos usando o sistema binário como base, mas como podemos representar uma imagem?

Do mesmo jeito que é feito com os caracteres, novamente, cada número representa uma core com base em uma tabela que foi acordada entre um grupo de pessoas. Você já deve ter ouvido falar de `RGB`, 
que significa red, green and blue (vermelho, verde e azul). Como é sabido que todas as cores do arcoíris conseguem ser representadas quando misturadas essas tres cores, este sistema sistema foi criado, e cada uma das
letras, representa a quantidade de cada cor a sua tela precisa misturar para criar a cor que é representada por um bite, ou seja um número binário composto por oito dígitos. que pode ir de 0 à 255.

> Exemplo de cores representadas pela tabela `RGB`:

````
rgb(0,0,0) = rgb(0000000,0000000,0000000) = Preto
rgb(255, 255, 255) = rgb(11111111, 11111111, 11111111) = Branco
````

E se você se pergunta por que existem tantas extenções de arquivos, como `.PNG`, `.GIF`, `.JPEG`, isso é somente um exemplo de mais um momento em que várias pessoas acordaram em como guardar e interpretar esses zeros e uns de maneiras um pouco diferentes, mas no fim, continuam ainda sendo somente zeros e uns.

E deste jeito, todos os tipos de dados, letras, emojis, imagens, vídeos, músicas são representados por um computador usando apenas os zeros e uns, fornecidos pelos impulsos elétricos que são passados pelos transistores.

# Algoritimos

Agora que já entendemos como é feita a representação de dados através de um sistema binário, como o computador transforma zeros e uns em letras, dígitos, emojis, imagens, videos e etc... Conseguimos entender melhor os  algoritimos que são usados para fazer isso. 

Percebemos que tudo que um computador faz, é usar uma entrada (input) e transformar em uma saída (output), porém, para que tenhamos a saída desejada, temos que desenvolver um algorítimo que usa a entrada e 
executa instruções a modo que, a saída do algoritimo esteja de acordo com o resultado que desejamos.

Pense numa receita culinária, por exemplo. Ela tem os ingredientes necessários (dados de entrada), passo a passo para realizar a receita (processamento ou instruções lógicas) e atinge um resultado (o prato finalizado). Conforme nossa receita fica mais complexa, com mais ingredientes, uma cobertura diferenciada, mais complexo ficará o nosso algoritimo, que deve levar em conta agora todos os ingredientes e passos a mais no momento do preparo.

> Entrada:

3 xícaras (chá) de Farinha de Trigo;
1 xícara (200 g) de manteiga em temperatura ambiente;  
2 xícaras (chá) de açúcar;  
4 ovos;  
1 xícara (chá) de leite;  
2 colheres (chá) de fermento em pó;  
1 pitada de sal;  
Manteiga e farinha de trigo para untar e polvilhar a forma;  
Açúcar de confeiteiro para polvilhar;  

> Algoritimo:  

1. Na batedeira, bata a manteiga até que ficar esbranquiçada. Adicione aos poucos o açúcar. Bata por cerca de 5 minutos.  
2. Junte os ovos, um a um, batendo sempre. Acrescente o sal e, em seguida, a Farinha de Trigo alternando com o leite.   
3. Desligue a batedeira e, por último, misture o fermento delicadamente com uma espátula. Transfira para a forma untada e enfarinhada.  
4. Leve ao forno preaquecido a 180°C e deixe assar por aproximadamente 40 minutos ou até que faça o teste de espetar o palito no centro do bolo e ele saia limpo.  
5. Desenforme e sirva.

> Saída:

🎂🎂🎂

Note que nosso algorítimo segue uma sequência lógica, bem definida, e nos instrui a executar um passo de cada vez no momento certo, para que o resultado final seja o esperado.

---

![dotnet](./.net.png)

# O C#

O C# é uma linguagem de programação moderna, orientada a objeto e `type-safe`. O C# permite que os desenvolvedores criem muitos tipos de aplicativos seguros, robustos e multiplataforma que são executados na plataforma .NET.  

Vários recursos do C# ajudam a criar aplicativos robustos e duráveis. A coleta de lixo recupera automaticamente a memória ocupada por objetos não utilizados. Os tipos nullables protegem contra variáveis que não se  referem a objetos alocados. A manipulação de exceção fornece uma abordagem estruturada e extensível para detecção e recuperação de erros. As expressões lambda dão suporte a técnicas de programação funcional.  

A sintaxe de linguagem deconsulta integrada (LINQ) cria um padrão comum para trabalhar com dados de qualquer fonte. A linguagem oferece suporte para operações assíncronas e fornece a sintaxe para a criação de sistemas distribuídos. 
  
O C# tem um sistema de tipos unificado. Onde todos os tipos do C#, incluindo tipos primitivos, como int e double, herdam de um único tipo de object raiz. Todos os tipos compartilham um conjunto de operações comuns.

Os valores de qualquer tipo podem ser armazenados, transportados e operados de maneira consistente. Além disso, o C# dá suporte a tipos de referência definidos pelo usuário e tipos de valor e permite a alocação dinâmica de objetos e o armazenamento em linha de estruturas leves. O C# oferece suporte a tipos e métodos genéricos, que fornecem aumento na segurança e no desempenho.

# O .Net

Os programas em C# são executados na plataforma .NET, um sistema de execução virtual chamado `Common Language Runtime` (CLR) e um conjunto de bibliotecas de classes. O CLR é a implementação da Microsoft da CLI (Common Language Infrastructure), um padrão internacional.  

A CLI é a base para a criação de ambientes de execução e desenvolvimento nos quais as linguagens e bibliotecas funcionam em conjunto diretamente.  

O código-fonte escrito em C# é compilado em uma `IL` (linguagem intermediária) que está de acordo com a especificação da CLI. O código de `IL` e os recursos, como bitmaps e cadeias de caracteres, são armazenados em um assembly, normalmente com uma extensão ".dll". Um assembly contém um manifesto que fornece informações sobre os tipos, a versão e a cultura do assembly.

Quando o programa C# é executado, o assembly é carregado no CLR. O CLR executa a compilação `JIT` (just-intime) para converter o código `IL` em instruções de máquina nativa. O CLR fornece outros serviços relacionados à coleta de lixo, manipulação de exceções e gerenciamento de recursos automáticos.

A interoperabilidade da linguagem é um recurso fundamental do .NET.   

O código de IL produzido pelo compilador está de acordo com a CTS (especificação de tipo comum). O código IL gerado do C# pode interagir com o código gerado nas versões do .NET do F#, Visual Basic, C++.

Há mais de 20 outros idiomas em conformidade com CTS. Um único assembly pode conter vários módulos escritos em diferentes linguagens .NET.

Os tipos podem referenciar um ao outro como se fossem escritos no mesmo idioma. Além dos serviços de tempo de execução, o .NET também inclui bibliotecas extensivas. Essas bibliotecas dão suporte a várias cargas de trabalho diferentes. Eles são organizados em namespaces que fornecem uma ampla variedade de funcionalidades úteis. As bibliotecas incluem tudo, desde entrada e saída de arquivo até a manipulação de cadeia de caracteres à análise de XML, aplicativos web e applicativos nativos do Windows.

###  Você pode criar aplicativos .NET para muitos sistemas operacionais, incluindo:

* Windows
* macOS
* Linux
* Android
* iOS
* tvOS
* watchOS

### As arquiteturas de processador com suporte incluem:

* x64
* x86
* ARM32
* ARM64

## Compilador JIT e IL

As linguagens .NET de nível mais alto , como C#, são compiladas em um conjunto de instruções independente de hardware, que é chamado de `IL` (linguagem intermediária).  

Quando um aplicativo é executado, o compilador `JIT` (just-in-time) converte a IL em código de computador que o processador entende. A compilação `JIT` ocorre no mesmo computador em que o código será executado.

Como a compilação `JIT` ocorre durante a execução do aplicativo, o tempo de compilação faz parte do tempo de execução. Portanto, os compiladores `JIT` têm que equilibrar o tempo gasto otimizando o código em 
relação à economia que o código resultante pode produzir. Mas um compilador `JIT` conhece o hardware real e pode liberar os desenvolvedores de ter que enviar implementações diferentes para diferentes plataformas.

O compilador `JIT` do .NET pode fazer a compilação em camadas, o que significa que ele pode recompilar métodos individuais em tempo de execução. Esse recurso permite que ele seja compilado rapidamente e 
ainda seja capaz de produzir uma versão altamente ajustada do código para métodos usados com frequência.

## Gerenciamento automático de memória

O `GC` (coletor de lixo) gerencia a alocação e a liberação de memória para aplicativos. Sempre que o código cria um novo objeto, o CLR aloca memória para o objeto do heap gerenciado. Desde que exista espaço de endereço
disponível no heap gerenciado, o runtime continua alocando espaço para novos objetos. Quando não há espaço de endereço livre suficiente, o `GC` verifica se há objetos no heap gerenciado que não estão mais sendo 
usados pelo aplicativo. Em seguida, ele recupera essa memória.

O `GC` é um dos serviços CLR que ajudam a garantir a segurança da memória. Um programa é considerado de memória segura se ele acessa somente a memória alocada. Por exemplo, o runtime garante que um aplicativo não
acesse memória não alocada além dos limites de uma matriz.

# .Net Core vs .Net Framework vs .Net Standard

![dotnet-structure](./estrutura-dotnet.png)

## .NET Framework

O .NET Framework surgiu em meados de 2002, ele era um framework único para desenvolvimento na plataforma Windows. Com o passar do tempo ganhou suporte para WEB, WCF, WPF, Windows Forms, etc, ele é composto por dois  componentes principais: O CLR (Common Language Runtime), o mecanismo de execução que manipula os aplicativos em execução, e a biblioteca de classes .NET Framework, que oferece uma biblioteca imensa de códigos 
testados e reutilizáveis.

Atualmente o .NET Framework está na versão 4.8 e não receberá mais atualizações com features adicionais, apenas será atendido com correções de bugs de segurança e confiabilidade.

## .NET Core

O .NET Core surgiu em meados de 2016, sua característica mais marcante é ele ser cross-plataform, isto é, ele é suportado em múltiplas plataformas, sendo possível o desenvolvimento em Windows, Linux e MacOS.

A Microsoft percebeu que não poderia ficar presa ao ambiente Windows, mas seria quase impossível reutilizar o até então .NET Framework. De uma maneira inteligente, foi iniciado um novo projeto, 
que iria andar em paralelo com a versão atual, mas com uma nova arquitetura, open-source e modular, surgiu então o dotnet core.

## .NET Standard

O .NET Standard, atualmente na versão 2.1, surge para ser um meio termo entre as duas versões, ele é uma interface que define a lista de APIs que uma determinada função do .NET deve suportar.
Sendo assim, uma biblioteca escrita utilizando o .NET Standard pode ser suportado tanto por aplicações utilizando o .NET Core quanto o .NET Framework. Ele foi criado para que esse compartilhamento seja muito mais fácil e uniforme no ecossistema do .NET. No entanto, vale lembrar, que com o advento do .NET 5, que será universal, a utilização dele se torna desnecessária em muitos cenários.

## Qual o futuro do .NET?

Em 2020 tivemos o lançamento do .NET 5, que não é mais o futuro, e sim o presente da plataforma .NET. Ambas as versões eram mantidas em paralelo, mas agora temos um ponto de encontro entre as duas versões, 
o .NET Framework 4.8, e .NET Core 3.1, são agora o .NET 5, e não teremos mais duas versões. O próximo lançamento está planejado para novembro de 2021, com o .NET 6. 

Se você está planejando construir uma nova aplicação utilizando o .NET, ela deve iniciar com o .NET 5, e para sistemas legados, que utilizam o .NET Framework, deve ser iniciado um planejamento para a migração,
visto que a Microsoft irá deprecear o .NET Framework.

![dotnet-roadmap](./roadmap-dotnet.png)

# CLI

O .Net oferece uma `CLI` (interface de linha de comando) para a gestão e controles de aplicativos desevolvidos na plataforma. 

A `CLI` do .NET é uma ferramenta multiplataforma para desenvolvimento, criação, execução e publicação de aplicativos .NET multiplataforma e é instalada por padrão na máquina onde está instalada o SDK do .Net Core.

### Comandos básicos do CLI

* new
* restore 
* build
* publish
* run
* test
* vstest
* pack
* migrate
* clean
* sln
* help
* store

### Comando

O comando executa uma ação. Por exemplo, `dotnet build` compila código, `dotnet publish` publica o código. 

Os comandos são implementados como um aplicativo de console usando uma convenção "dotnet {command}".

### Argumentos

Os argumentos que você passa na linha de comando são aqueles do comando invocado. 

Por exemplo, quando você executa `dotnet publish my_app.csproj`, o `my_app.csproj` é o argumento que indica o projeto a ser publicado e é passado para o comando `publish` como parâmetro.

### Opções

As opções que você passa na linha de comando são aquelas do comando invocado. 

Por exemplo, quando você executa `dotnet publish --output /build_output`, a opção `--output` e seu valor são passados para o comando `dotnet publish`.

# Software livre

O .NET é de código aberto, usando licenças MIT e Apache 2. O .NET é um projeto do .NET Foundation.
Para obter mais informações, consulte a lista de repositórios de projeto no [github](https://github.com/dotnet/core/blob/main/Documentation/core-repos.md).

# IDEs

### Visual Studio

A Microsoft desenvolve e fornece uma das IDEs mais completas e ultilizadas para o desenvolvimento na plataforma .Net, o Visual Studio, que pode ser baixada e utilizada de graça por desenvolvedores por período inderterminado.

### Visual Studio Code

A Microsoft também desenvolveu uma IDE mais leve e de código aberto, totalmente gratuíta que ficou muito famosa ultimamente por seus variados plugins que dão suporte a basicamente qualquer linguagem de programação em um pacote mais leve 
e personalizável.

---

# Variáveis

As variáveis representam locais de armazenamento. Cada variável tem um tipo que determina quais valores podem ser armazenados na variável. O C# é uma linguagem de tipo seguro, e o compilador garante que os valores armazenados em variáveis sejam sempre do tipo apropriado. O valor de uma variável pode ser alterado por atribuição ou pelo uso de operadores.

> Uma variável deve ser definitivamente atribuída (atribuição definitiva) antes que seu valor possa ser obtido.

O C# define sete categorias de variáveis: `variáveis estáticas`, `variáveis de instância`, `elementos de matriz`, `parâmetros de valor`, `parâmetros de referência`, `parâmetros de saída` e `variáveis locais`.

### Variáveis estáticas:

Um campo declarado com o modificador `static` é chamado de uma variável estática. Uma variável estática entra em existência no momento da criação do aplicativo, e deixa de existir quando o domínio do aplicativo associado deixar de existir.

### Variáveis de instância:

Um campo declarado sem o modificador `static` é chamado de variável de instância.

#### Variável de instância de uma classe:

Uma variável de instância de uma classe entra em existência quando uma nova instância dessa classe é criada, e deixa de existir quando não há nenhuma referência a essa instância.

#### Variáveis de instância em structs:

Uma variável de instância de uma struct tem exatamente o mesmo tempo de vida que a variável de struct à qual ela pertence. Em outras palavras, quando uma variável de um tipo struct entra em existência ou deixa de existir, também as variáveis de instância do struct.

### Elementos de matriz:

Os elementos de uma matriz entram em existência quando uma instância de matriz é criada e deixam de existir quando não há mais nenhuma referência a essa instância de matriz.

### Parâmetros de valor:

Um parâmetro declarado sem um modificador `ref` ou `out` é um parâmetro de valor.

Um parâmetro de valor entra em existência na invocação do membro da função (método, construtor), e é inicializado com o valor do argumento fornecido na invocação.
Um parâmetro de valor normalmente deixa de existir no retorno do membro da função ou da função anônima.

### Parâmetros de referência:

Um parâmetro declarado com um modificador `ref` é um parâmetro de referência.

Um parâmetro de referência não cria um novo local de armazenamento (registro na memória). Em vez disso, um parâmetro de referência representa o mesmo local de armazenamento que a variável fornecida como o argumento no membro da função. Assim, o valor de um parâmetro de referência é sempre o mesmo que a variável subjacente.

### Parâmetros de saída:

Um parâmetro declarado com um modificador `out` é um parâmetro de saída.

Parecido com um parametro de referência, um parâmetro de saída não cria um novo local de armazenamento. Em vez disso, um parâmetro de saída representa o mesmo local de armazenamento que a variável fornecida como o argumento no membro da função. Assim, o valor de um parâmetro de saída é sempre o mesmo que a variável subjacente.

### Variáveis locais:

Uma variável local é declarada por uma declaração simples, que pode ocorrer em um bloco, como dentro de um for, switch, using, foreach, try/catch...

O tempo de vida de uma variável local é a parte da execução do programa durante o qual o armazenamento tem a garantia de ser reservado para ele. Esse tempo de vida se estende pelo menos da entrada do bloco,
o qual está associado, até a execução desse bloco.
Se o bloco pai, for inserido recursivamente, uma nova instância da variável local será criada a cada vez.

> Uma variável local não é inicializada automaticamente e, portanto, não tem valor padrão.

Para declarar uma varíavel local, podemos usar a palavra-chave `var`, ou explicitamente definir o tipo da variável antes de atribuir um valor a ela. Como no exemplo a seguir:

````
var a = 1; 
int b = 2;
````

Também pode se declarar várias variáveis do mesmo tipo em uma só linha:

````
int a = 1, b = 2, c = 3;
````

###### Constantes:

Se você quer ter certeza que o valor da sua variável **não seja modificado** em nenhuma parte do código após a declaração do seu valor, deve se usar a palavra-chave `const`, que proíbe que o valor da variável seja alterado pelo programa após sua inicialização:

````
const int a = 1;
````

# Operadores

Toda linguagem de programação possui operadores lógicos para realizar operações booleanas, que resultam em `verdadeiro` ou `falso`, esses operadores se diferem somente no jeito que são definidos pela sintaxe de cada linguagem de programação, mas servem o mesmo propósito e são muito utilizadas por qualquer programa.

### Operadores lógicos:

#### Operador NOT: `!`

O operador `!` calcula a negação lógica de seu operando. Ou seja, ele produz verdadeiro, se o operando for avaliado como falso, e falso, se o operando for avaliado como verdadeiro:

````
using System;
					
public class Program
{
	public static void Main()
	{		
		Console.WriteLine(!false);  // Saída: True
		Console.WriteLine(!true);   // Saída: False
	}
}
````

#### Operador AND: `&`, `&&`

O operador `&` computa o AND lógico de seus operandos. O resultado de `x & y` será verdadeiro se ambos `x` e `y` forem avaliados como verdadeiros. Caso contrário, o resultado será falso:

O operador AND lógico condicional `&&` também computa o AND lógico e seus operandos, **mas não avalia o operando à direita se o operando à esquerda for avaliado como falso**:

````
using System;
					
public class Program
{
	public static void Main()
	{		
		Console.WriteLine(false & false); // Saída: False
		Console.WriteLine(true & false);  // Saída: False
		Console.WriteLine(false && true); // Saída: False
		Console.WriteLine(true & true);   // Saída: True
	}
}
````

#### Operador OR: `|`, `||`, `^`

O operador `^` computa o OR exclusivo lógico, também conhecido como o XOR lógico, de seus operandos. O resultado de `x ^ y` é verdadeiro se `x` é avaliado como verdadeiro e `y` avaliado como falso, ou `x` avaliado como falso e `y` avaliado como verdadeiro. Caso contrário, o resultado será falso. Ou seja, o operador `^` calcula o mesmo resultado que o operador de desigualdade `!=`:

````
using System;
					
public class Program
{
	public static void Main()
	{		
		Console.WriteLine(true ^ true);    // Saída: False
		Console.WriteLine(true ^ false);   // Saída: True
		Console.WriteLine(false ^ true);   // Saída: True
		Console.WriteLine(false ^ false);  // Saída: False
	}
}
````

O operador `|` computa o OR lógico de seus operandos. O resultado de `x | y` será true se `x` ou `y` for avaliado como verdadeiro. Caso contrário, o resultado será falso:

````
using System;
					
public class Program
{
	public static void Main()
	{		
		Console.WriteLine(true | true);    // Saída: True
		Console.WriteLine(true | false);   // Saída: True
	}
}
````

O operador `||` também computa o OR lógico e seus operandos, **mas não avalia o operando à direita se o operando à esquerda for avaliado como verdadeiro**:

````
using System;
					
public class Program
{
	public static void Main()
	{		
		Console.WriteLine(true || true);    // Saída: True
		Console.WriteLine(true || false);   // Saída: True
	}
}
````

#### Precedência dos operadores lógicos

A lista a seguir ordena os operadores lógicos, começando da mais alta precedência até a mais baixa:

1. Operador de negação lógica `!`
2. Operador AND lógico `&`
3. Operador OR exclusivo lógico `^`
4. Operador OR lógico `|`
5. Operador AND lógico condicional `&&`
6. Operador OR lógico condicional `||`

> Use parênteses para alterar a ordem de avaliação imposta pela precedência do operador.

### Operadores aritméticos

#### Operador de incremento: `++`

O operador de incremento unário `++` incrementa seu operando em 1. O operando precisa ser uma variável, um acesso de propriedade ou um acesso de indexador:

````
using System;
					
public class Program
{
	public static void Main()
	{		
		int i = 3;
		Console.WriteLine(i);  // Saída: 3
		i++;
		Console.WriteLine(i);  // Saída: 4
	}
}
````

#### Operador de decremento: `--`

O operador de decremento unário `--` decrementa o operando em 1. O operando precisa ser uma variável, um acesso de propriedade ou um acesso de indexador:

````
using System;
					
public class Program
{
	public static void Main()
	{		
		int i = 3;
		Console.WriteLine(i);  // Saída: 3
		i--;
		Console.WriteLine(i);  // Saída: 2
	}
}
````

#### Operador de multiplicação: `*`

O operador de multiplicação `*` calcula o produto dos operandos:

````
using System;
					
public class Program
{
	public static void Main()
	{		
		Console.WriteLine(5 * 2);         // Saída: 10
		Console.WriteLine(0.5 * 2.5);     // Saída: 1.25
		Console.WriteLine(0.1m * 23.4m);  // Saída: 2.34
	}
}
````

#### Operador de divisão: `/`

O operador de divisão `/` divide o operando à esquerda pelo operando à direita:

````
using System;
					
public class Program
{
	public static void Main()
	{		
		Console.WriteLine(13 / 5);    // Saída: 2
		Console.WriteLine(-13 / 5);   // Saída: -2
		Console.WriteLine(13 / -5);   // Saída: -2
		Console.WriteLine(-13 / -5);  // Saída: 2
	}
}
````

#### Operador de resto: `%`

O operador de resto `%` calcula o resto após dividir o operando à esquerda pelo à direita:

````
using System;
					
public class Program
{
	public static void Main()
	{		
		Console.WriteLine(5 % 4);   // Saída: 1
		Console.WriteLine(5 % -4);  // Saída: 1
		Console.WriteLine(-5 % 4);  // Saída: -1
		Console.WriteLine(-5 % -4); // Saída: -1
	}
}
````

#### Operador de adição: `+`

O operador de adição `+` calcula a soma dos operandos:

````
using System;
					
public class Program
{
	public static void Main()
	{		
		Console.WriteLine(5 + 4);       // Saída: 9
		Console.WriteLine(5 + 4.3);     // Saída: 9.3
		Console.WriteLine(5.1m + 4.2m); // Saída: 9.3
	}
}
````

#### Operador de subtração: `-`

O operador de subtração `-` subtrai o operando à direita do operando à esquerda:

````
using System;
					
public class Program
{
	public static void Main()
	{		
		Console.WriteLine(47 - 3);      // Saída: 44
		Console.WriteLine(5 - 4.3);     // Saída: 0.7
		Console.WriteLine(7.5m - 2.3m); // Saída: 5.2
	}
}
````

#### Precedência e associatividade dos operadores

A seguinte lista ordena os operadores aritméticos da precedência mais alta para a mais baixa:

1. Operadores de multiplicação, divisão e resto: `*`, `/` e `%`
2. Operadores de adição e subtração: `+` e `-`

> Operadores aritméticos binários são associativos à esquerda. Ou seja, os operadores com o mesmo nível de precedência são avaliados da esquerda para a direita.

> Use parênteses para alterar a ordem de avaliação imposta pela precedência e pela capacidade de associação do operador.

### Operadores de igualdade

#### Operador de igualdade: `==`

O operador de igualdade `==` retornará verdadeiro se seus operandos forem iguais, caso contrário, falso:

````
using System;
					
public class Program
{
	public static void Main()
	{				
		Console.WriteLine(1 == 1);      // Saída: True
		Console.WriteLine(1 == 10);     // Saída: False
		Console.WriteLine("x" == "x");  // Saída: True		
	}
}
````

#### Operador de desigualdade: `!=`

O operador de desigualdade `!=` retornará verdadeiro se seus operandos não forem iguais, caso contrário, falso:

````
using System;
					
public class Program
{
	public static void Main()
	{				
		Console.WriteLine(1 != 1);      // Saída: False
		Console.WriteLine(1 != 10);     // Saída: True
		Console.WriteLine("x" != "x");  // Saída: False		
	}
}
````

### Operadores de comparação

#### Operador menor que: `<`

O operador `<` retornará verdadeiro se o operando à esquerda for menor do que o operando à direita, caso contrário, falso:

````
using System;
					
public class Program
{
	public static void Main()
	{				
		Console.WriteLine(7.0 < 5.1);   // Saída: False
		Console.WriteLine(5.1 < 5.1);   // Saída: False
		Console.WriteLine(0.0 < 5.1);   // Saída: True
	}
}
````

#### Operador maior que: `>`

O operador `>` retornará verdadeiro se o operando à esquerda for maior do que o operando à direita, caso contrário, falso:

````
using System;
					
public class Program
{
	public static void Main()
	{				
		Console.WriteLine(7.0 > 5.1);   // Saída: True
		Console.WriteLine(5.1 > 5.1);   // Saída: False
		Console.WriteLine(0.0 > 5.1);   // Saída: False
	}
}
````

#### Operador menor ou igual `<=`

O operador `<=` retornará true se o operando à esquerda for menor ou igual ao operando à direita, caso contrário, false:

````
using System;
					
public class Program
{
	public static void Main()
	{				
		Console.WriteLine(7.0 <= 5.1);   // Saída: False
		Console.WriteLine(5.1 <= 5.1);   // Saída: True
		Console.WriteLine(0.0 <= 5.1);   // Saída: True
	}
}
````

#### Operador maior ou igual `>=`

O operador `>=` retornará true se o operando à esquerda for maior ou igual ao operando à direita, caso contrário, false:

````
using System;
					
public class Program
{
	public static void Main()
	{				
		Console.WriteLine(7.0 >= 5.1);   // Saída: True
		Console.WriteLine(5.1 >= 5.1);   // Saída: True
		Console.WriteLine(0.0 >= 5.1);   // Saída: False
	}
}
````

### Operadores ternários:

#### Operador ternário: `?`

O operador condicional, também conhecido como operador condicional ternário, avalia uma expressão booleana e retorna o resultado de uma das duas expressões, dependendo se a expressão booleana é avaliada, como mostra o exemplo:

````
using System;
					
public class Program
{
	public static void Main()
	{				
		
		Console.WriteLine(BuscaDescricaoTemperatura(15));  // output: Frio
		Console.WriteLine(BuscaDescricaoTemperatura(27));  // output: Perfeito
		
        string BuscaDescricaoTemperatura(double temperatura) => temperatura < 20.0 ? "Frio" : "Perfeito";
	}
}
````

Como mostra o exemplo anterior, a sintaxe do operador condicional é a seguinte:

> condicao ? consequência : alternativa

# Instruções

As ações que um programa executa são expressas em instruções. Ações comuns incluem declarar variáveis, atribuir valores, chamar métodos, fazer loops pelas coleções e ramificar para um ou para outro bloco de código, dependendo de uma determinada condição. A ordem na qual as instruções são executadas em um programa é chamada de fluxo de controle ou fluxo de execução. O fluxo de controle pode variar sempre que um programa é
executado, dependendo de como o programa reage às entradas que recebe em tempo de execução.

Uma instrução pode consistir em uma única linha de código que termina em um ponto e vírgula, ou uma série de instruções de uma linha em um bloco. 

## Instruções de seleção

#### A instrução `if`

É uma instrução que define `se` determinado bloco de código deve ser executado com base no resultado de uma expressão booleana, como mostra o exemplo a seguir:

````
using System;
					
public class Program
{
	public static void Main()
	{				
		double temperatura = 20.0;
		if (temperatura < 20.0)
		{
       		Console.WriteLine("Frio");
    	}
        else
    	{
        	Console.WriteLine("Perfeito");
    	}
	}	
}
````

Uma instrução `if` pode não vir acompanhada de uma instrução `else`:

````
using System;
					
public class Program
{
	public static void Main()
	{			
		int valor = 250;

		if (valor < 0 || valor > 100)
        {
            Console.Write("Valor muito baixo ou muito alto");
        }

    	Console.WriteLine($"O valor é {valor}");
	}	
}
````

Você pode aninhar instruções `if` para verificar várias condições:

````
using System;

public class Program
{
	public static void Main()
	{
		char ch = 'a';
		if (char.IsUpper(ch))
		{
			Console.WriteLine($"É uma letra maíuscula: {ch}");
		}
		else if (char.IsLower(ch))
		{
			Console.WriteLine($"É uma letra minúscula: {ch}");
		}
		else if (char.IsDigit(ch))
		{
			Console.WriteLine($"É um dígito: {ch}");
		}
		else
		{
			Console.WriteLine($"Não é um caracter alfanumérico: {ch}");
		}
	}
}
````

#### A instrução `switch`

A instrução `switch` seleciona uma lista de instruções a ser executada com base em uma combinação de padrões com uma expressão de match:

````
using System;

public class Program
{
	public static void Main()
	{
		double medida = 2;
		switch (medida)
		{
			case < 0.0:
				Console.WriteLine($"Valor medido é: {medida}; muito baixo.");
				break;
			case > 15.0:
				Console.WriteLine($"Valor medido é: {medida}; muito alto.");
				break;
			case double.NaN:
				Console.WriteLine("Inválido");
				break;
			default:
				Console.WriteLine($"Valor medido é: {medida}.");
				break;
		}
	}
}
````

Você pode especificar vários padrões de `case` para uma seção de valores:

````
using System;

public class Program
{
	public static void Main()
	{
		double medida = 2;
		switch (medida)
		{
			case <0:
			case>100:
				Console.WriteLine($"Valor medido é: {medida}; fora do intervalo aceito.");
				break;
			default:
				Console.WriteLine($"Valor medido é: {medida}.");
				break;
		}
	}
}
````

Uma expressão simples de `case` pode não ser o suficiente para especificar a condição para a execução do bloco de código. Nesse caso, você pode usar um `case guard`. Essa é uma condição adicional que deve ser atendida junto com um padrão de combinação. Um `case guard` deve ser uma expressão booleana. Especifique um `case guard` após a palavra-chave `when`, como mostra o exemplo a seguir:

````
using System;

public class Program
{
	public static void Main()
	{
		int a = 4, b = 3;
		switch ((a, b))
		{
			case (>0, >0) when a == b:
				Console.WriteLine($"Os doi valores são validos e iguais a: {a}.");
				break;
			case (>0, >0):
				Console.WriteLine($"Primeiro valor é: {a}, segundo valor é: {b}.");
				break;
			default:
				Console.WriteLine("Um ou todos os valores são inválidos");
				break;
		}
	}
}
````

## Instruções de iteração

#### A instrução `do while`

A instrução `do while` executa uma instrução ou um bloco de instruções enquanto uma expressão booleana é avaliada como verdadeira. Como essa expressão é avaliada após cada execução do loop, um loop `do while`
é executado uma ou mais vezes. Isso é diferente de um loop while, que executa zero ou mais vezes:

````
using System;

public class Program
{
	public static void Main()
	{
		int n = 0;
		do
		{
			Console.Write(n);
			n++;
		}
		while (n < 5);
	}
}
````

#### A instrução `while`

A instrução `while` executa uma instrução ou um bloco de instruções enquanto uma expressão booleana especificada é avaliada como verdadeira. Como essa expressão é avaliada antes de cada execução do loop, um loop while é executado zero ou mais vezes:

````
using System;

public class Program
{
	public static void Main()
	{
		int n = 0;
		while (n < 5)
		{
			Console.Write(n);
			n++;
		}
	}
}
````

#### A instrução `for`

A instrução `for` executa uma instrução ou um bloco de instruções enquanto uma expressão booleana especificada é avaliada como verdadeira. O exemplo a seguir mostra a instrução `for` que executa seu corpo
enquanto um contador inteiro é menor que três:

````
using System;

public class Program
{
	public static void Main()
	{
		for (int i = 0; i < 3; i++)
		{
			Console.Write(i);
		}
	}
}
````

#### A instrução `foreach`

A instrução `foreach` executa uma instrução ou um bloco de instruções para cada elemento em uma instância do tipo que implementa a interface ou, como mostra o foreach exemplo a `System.Collections.IEnumerable<T>`:

````
using System;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var sequenciaFibonacci = new List<int>{0, 1, 1, 2, 3, 5, 8, 13};
		foreach (int numero in sequenciaFibonacci)
		{
			Console.Write($"{numero} ");
		}
	}
}
````

## Instruções de atalho

### Return

A instrução `return` finaliza a execução do método em que aparece e retorna o controle para o método de chamada. Ela também pode retornar um valor opcional. Se o método for um tipo void, a instrução `return`
poderá ser omitida.

Se a instrução `return` estiver dentro de um bloco try, o bloco finally, se houver, será executado antes que o controle retorne para o método de chamada.

No exemplo a seguir, o método `CalculateArea()` retorna a variável local `area` como um valor double:

````
using System;

public class Program
{
	public static void Main()
	{
		int radius = 5;
		double result = CalculateArea(radius);
		Console.WriteLine("The area is {0:0.00}", result);
		Console.ReadKey();
	}

	static double CalculateArea(int r)
	{
		double area = r * r * Math.PI;
		return area;
	}
}
````

### Continue

A instrução `continue` passa o controle para a próxima iteração da instrução de iteração delimitadora na qual ele aparece.

Neste exemplo, um contador é inicializado para a contagem de 1 a 10. Usando a instrução `continue` em conjunto com a expressão (i< 9), as instruções entre `continue` e o final do bloco `for` são ignoradas nas
iterações em que i é menor que 9. Nas duas últimas iterações do loop `for` (onde i == 9 e i == 10), a instrução `continue` não é executada e o valor de i é impresso no console.

````
using System;

public class Program
{
	public static void Main()
	{
		for (int i = 1; i <= 10; i++)
		{
			if (i < 9)
			{
				continue;
			}

			Console.WriteLine(i);
		}

		Console.ReadKey();
	}
}
````

### Break

A instrução `break` encerra o loop delimitado mais próximo, ou switch na qual ela aparece. O controle é passado para a instrução que segue a instrução encerrada, se houver.

Neste exemplo, a instrução condicional tem um contador que deveria contar de 1 a 100. No entanto, a instrução `break` encerra o loop após 4 contagens.

````
using System;

public class Program
{
	public static void Main()
	{
		for (int i = 1; i <= 100; i++)
		{
			if (i == 5)
			{
				break;
			}

			Console.WriteLine(i);
		}

		Console.ReadKey();
	}
}
````

## Instruções para tratamento de exceções

### Throw

A sintaxe de throw é:

> throw [e];

Em que `e` é uma instância de uma classe derivada de `System.Exception`. O exemplo a seguir usará a instrução `throw` para gerar um `IndexOutOfRangeException` se o argumento passado para o método chamado
GetNumber não corresponder a um índice válido de uma matriz interna.

````
public class NumberGenerator
{
    int[] numbers = { 2, 4, 6, 8, 10, 12, 14, 16, 18, 20 };

    public int GetNumber(int index)
    {
        if (index < 0 || index >= numbers.Length)
        {
            throw new IndexOutOfRangeException();
        }

        return numbers[index];
    }
}
````
Os chamadores do método, então, usam um bloco `try-catch` ou `try-catch-finally` para tratar a exceção gerada. 

O exemplo a seguir trata a exceção gerada pelo método GetNumber:

````
public static void Main()
{
    var gen = new NumberGenerator();
    int index = 10;
    try
    {
        int valor = gen.GetNumber(index);
        Console.WriteLine($"Recuperado: {valor}");
    }
    catch (IndexOutOfRangeException e)
    {
        Console.WriteLine($"{e.GetType().Name}: {index} está fora dos limites do array");
    }
}
````

### Try-Catch

A instrução `try-catch` consiste em um bloco `try` seguido por uma ou mais cláusulas `catch`, que especificam os manipuladores para diferentes exceções. Quando uma exceção é lançada, o CLR (Common Language Runtime) procura a instrução catch que trata essa exceção. Se o método em execução no momento não contiver um bloco `catch`, o CLR procurará no método que chamou o método atual e assim por diante para cima na pilha de chamadas. Se nenhum bloco `catch` for encontrado, o CLR exibirá uma mensagem de exceção sem tratamento para o usuário e interromperá a execução do programa.

O bloco `try` contém o código protegido que pode causar a exceção. O bloco é executado até que uma exceção seja lançada ou ele seja concluído com êxito. Por exemplo, a tentativa a seguir de converter um objeto null
gera a exceção `NullReferenceException`:

````
using System;

public class Program
{
	public static void Main()
	{
		object o2 = "obj";
		try
		{
			int i2 = (int)o2; // Error
		}
		catch (InvalidCastException e)
		{
		}
	}
}
````

Embora a cláusula `catch` possa ser usada sem argumentos para capturar qualquer tipo de exceção, esse uso não é recomendado. Em geral, você deve capturar apenas as exceções das quais você sabe se recuperar.

É possível usar mais de uma cláusula `catch` específica na mesma instrução `try-catch`. Nesse caso, a ordem das cláusulas `catch` é importante porque as cláusulas `catch` são examinadas em ordem. Capture as exceções mais específicas antes das menos específicas:

````
catch (ArgumentException e) when (e.ParamName == "…")
{
}
````

Você pode capturar uma exceção e lançar uma exceção diferente. Quando fizer isso, especifique a exceção capturada como a exceção interna, como mostrado no exemplo a seguir:

````
catch (InvalidCastException e)
{
    throw new YourCustomException("Mensagem de erro.", e);
}
````

### Try-Finally

Usando um bloco `finally`, você pode limpar todos os recursos alocados em um bloco `try` e pode executar código mesmo se uma exceção ocorrer no bloco `try`. Normalmente, as instruções de um bloco `finally` são
executadas quando o controle deixa uma instrução `try`. A transferência decontrole pode ocorrer como resultado da execução normal, da execução de uma instrução break, continue, goto ou return, ou da
propagação de uma exceção para fora da instrução `try`.

> Dentro de uma exceção tratada, é garantido que o bloco finally será executado. No entanto, se a exceção não for tratada, a execução do bloco finally depende de como a operação de desenrolamento da exceção é
disparada. Isso, por sua vez, depende da configuração do seu computador. Os únicos casos em que as finally cláusulas não são executadas envolvem um programa que está sendo imediatamente interrompido.

````
using System;

public class Program
{
	public static void Main()
	{
		object obj = "obj";
		try
		{
			// Conversão inválida
			var i = (int)obj;

			// Esse código nunca é executado
			Console.WriteLine("Código que não é executado");
		}
		finally
		{
			Console.WriteLine("Código executado dentro do bloco finally");
		}
	}
}
````

### Try-Catch-Finally

Um uso comum de `catch` e `finally` juntos é obter e usar recursos em um bloco `try`, lidar com circunstâncias excepcionais em um bloco `catch` e liberar os recursos no bloco `finally`.

````
void ReadFile(int index)
{
    // To run this code, substitute a valid path from your local machine
    string path = @"c:\temp\test.txt";
    System.IO.StreamReader file = new System.IO.StreamReader(path);
    char[] buffer = new char[10];
    try
    {
        file.ReadBlock(buffer, index, buffer.Length);
    }
    catch (System.IO.IOException e)
    {
        Console.WriteLine("Erro ao ler de {0}. Mensagem = {1}", path, e.Message);
    }
    finally
    {
        if (file != null)
        {
            file.Close();
        }
    }
}
````

---

# Tipos de dados

## Char

O .NET usa o Char para representar caracteres Unicode usando a codificação UTF-16. O valor de um Char é seu valor numérico de 16 bits (ordinal).

### Trabalhando com chars

Definindo uma variável do tipo char:

````
char chr = 'a';
````

````
var chr = 'a';
````

````
var chr = "\u0061";
````

````
char chr = (char)65;
````

#### O .Net oferece várias extensões para lidarmos com strings, contar os caracteres, separar, alterar, juntar, substituir e etc:

Quando necessitamos verificar se um char é um digito ou um caracter, usamos a função `IsDigit`:

````
using System;

public class Program
{
	public static void Main()
	{
		char letra = 'a';
		char digito = '1';
		Console.WriteLine(char.IsDigit(digito)); // Saída: True
		Console.WriteLine(char.IsDigit(letra)); // Saída: False
	}
}
````

#### Conversores (Parse, TryParse, Convert);

> Parse: 

````
using System;

public class Program
{
	public static void Main()
	{
		string str = "1";
		char chr = char.Parse(str);
		Console.WriteLine(chr); // Saída: 1
	}
}
````

> TryParse:

````
using System;

public class Program
{
	public static void Main()
	{
		string str = "a";
		if (char.TryParse(str, out char chr))
		{
			Console.WriteLine($"Valor convertido: {chr}"); // Saída: Valor convertido: a
		}
	}
}
````

> Convert

````
using System;

public class Program
{
	public static void Main()
	{
		string str = "A";
		char chr = Convert.ToChar(str);
		Console.WriteLine(chr); // Saída: A
	}
}
````

## String

Representa uma cadeia de caracteres, uma coleção de caracteres que é usada para representar um texto. Um objeto string é uma coleção sequencial de objetos `System.Char`. Um objeto `System.Char` corresponde a uma unidade de código UTF-16.

O valor do objeto string é o conteúdo da coleção sequencial de objetos `System.Char` e esse valor é imutável (ou seja, é somente leitura).

> O tamanho máximo de uma string na memória é de 2 GB ou cerca de 1.000.000.000 caracteres.

### Trabalhando com strings

Você pode criar uma string de várias maneiras diferentes, como:

Definindo uma variável do tipo string:

````
string str = "Uma string";
````

````
char[] chars = { 's', 't', 'r', 'i', 'n', 'g' };
string str = new string(chars);
````

````
string str = "Hoje é " + DateTime.Now.ToString("D") + ".";
````

#### O .Net oferece várias extensões para lidarmos com strings, contar os caracteres, separar, alterar, juntar, substituir e etc:

Quando precisamos somente de um pedaço de uma string, usamos a função `Substring`:

````
using System;

public class Program
{
	public static void Main()
	{
		string nome = "John Doe";
		string primeiroNome = nome.Substring(0, 4);
		string segundoNome = nome.Substring(5, 3);
		
		Console.WriteLine(primeiroNome); // Saída: John
		Console.WriteLine(segundoNome);  // Saída: Doe
	}
}
````
Quando precisamos juntar duas strings, podemos usar a função `Concat`:

````
using System;

public class Program
{
	public static void Main()
	{
		string primeiroNome = "John";
		string segundoNome = "Doe";
		string nomeCompleto = string.Concat(primeiroNome, " ", segundoNome);
		Console.WriteLine(nomeCompleto); // Saída: John Doe
	}
}
````

Quando precisamos juntar um array de elementos em uma única string, podemos usar a função `Join`:

````
using System;

public class Program
{
	public static void Main()
	{
		int[] valores = {1, 2, 4, 5, 6, 7, 8, 9, 10};
		string texto = string.Join(" ", valores);
		Console.WriteLine(texto);  // Saída: 1 2 3 4 5 6 7 8 9 10
	}
}
````

Para remover um pedaço do texto, podemos usar a função `Remove`:

````
using System;

public class Program
{
	public static void Main()
	{
		string texto = "John Doe";
		string primeiroNome = texto.Remove(4, 4);
		Console.WriteLine(primeiroNome); // Saída: John
	}
}
````

Para substituir uma letra, palavra ou pedaços de uma frase, podemos usar a função `Replace`

````
using System;

public class Program
{
	public static void Main()
	{
		string texto = "John Doe";
		string textoNormalizado = texto.Replace('o', 'a');
		Console.WriteLine(textoNormalizado); // Saída: Jahn Dae
	}
}
````

Para transformar um texto delimitado por algum caracter específico, e transformá-lo em um array de string, usamos a função `Split`

````
using System;

public class Program
{
	public static void Main()
	{
		string texto = "John,Doe";
		string[] textoSeparado = texto.Split(',');
		Console.WriteLine(textoSeparado[0]);  // Saída: John
		Console.WriteLine(textoSeparado[1]);  // Saída: Doe
	}
}
````

Para limparmos espaços em branco no início e no final de uma string, usamos a função `Trim`:

````
using System;

public class Program
{
	public static void Main()
	{
		string texto = "    John Doe   ";
		string textoSemEspacos = texto.Trim();
		Console.WriteLine(textoSemEspacos);    // Saída: John Doe
	}
}
````

> A função `Trim` também pode ser usada para remover os espaços em branco somente no início ou no final de uma string, usando suas variantes `TrimStart` e `TrimEnd` respectivamente.

Quando precisamos concatenar uma string, podemos usar também a interpolação de strings, adicionando o caracter `$` no começo da string:

````
using System;

public class Program
{
	public static void Main()
	{
		string primeiroNome = "John";
		string segundoNome = "Doe";
		string nomeCompleto = $"{primeiroNome} {segundoNome}";
		Console.WriteLine(nomeCompleto);  // Saída: John Doe
	}
}
````

Quando precisamos concatenar uma string a partir de varias variáveis de uma maneira organizada, também podemos usar a função `Format`:

````
using System;

public class Program
{
	public static void Main()
	{
		string primeiroNome = "John";
		string segundoNome = "Doe";
		string nomeCompleto = string.Format("{0} {1}", primeiroNome, segundoNome);
		Console.WriteLine(nomeCompleto);  // Saída: John Doe
	}
}
````

Quando temos um texto muito extenso, que precisamos pular uma linha na IDE para tornar o código mais legível, podemos usar o caracter `@` no começo de uma string:

````
using System;

public class Program
{
	public static void Main()
	{
		string texto = @"
			Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
			sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.";

		Console.WriteLine(texto);
	}
}
````

## Integer

Um integer é uma representação numérica de um número inteiro, e pode ser representado por um Int32, ou um Int64, os números `32` e `64` representam o numero de bytes que cada tipo pode alocar na memória.

Int32 é um tipo que representa os inteiros com sinal com valores que variam de `-2.147.483.648 ` até `2.147.483.647`.

Já o Int64 pode conter valores que variam de `-9.223.372.036.854.775.808` até `9.223.372.036.854.775.807`.

Dentro dos números inteiros também temos os UInt32 e UInt64, que seguem o mesmo comportamento dos inteiros comuns, porém só podem assumir valores positivos maiores que zero.

### Trabalhando com inteiros

Definindo uma variável do tipo inteiro:

````
Int32 inteiro = 0; // define uma varável do tipo Int32
````

````
Int64 inteiro = 0; // define uma varável do tipo Int64
````

````
int inteiro = 0; // quando omitido o tamanho, por padrão é definida uma varável do tipo Int32
````

````
var numero = 10; // por padrão, sempre quando inicianmos uma variável sem especificar o seu tipo, é definida uma variável do tipo Int32 por padrão
````

#### Conversores (Parse, TryParse, Convert);

> Parse: 

````
using System;

public class Program
{
	public static void Main()
	{
		string numeroStr = "10";
		int numero = int.Parse(numeroStr);
		Console.WriteLine(numero); // Saída: 10
	}
}
````

> TryParse:

````
using System;

public class Program
{
	public static void Main()
	{
		string numeroStr = "10";
		if (int.TryParse(numeroStr, out int numero))
		{
			Console.WriteLine($"Valor convertido: {numero}"); // Saída: Valor convertido: 10
		}
	}
}
````

> Convert

````
using System;

public class Program
{
	public static void Main()
	{
		string numeroStr = "10";
		int numero = Convert.ToInt32(numeroStr);
		Console.WriteLine(numero); // Saída: 10
	}
}
````

## Decimal

O tipo Decimal representa números decimais, com vírgula, que variam de `79228162514264337593543950335` a `-79228162514264337593543950335`.  

O tipo Decimal é apropriado para cálculos financeiros, que exigem um grande número de dígitos inteiros e fracionários significativos e nenhum erro de arredondamento.

### Trabalhando com decimais

Definindo uma variável do tipo decimal:

````
decimal numero = 1;
````

````
decimal numero = 2.5;
````

````
var numero = 2M;
````

> Note o uso do `M` para definir um decimal usando uma variável anônima

#### Conversores (Parse, TryParse, Convert);

> Parse: 

````
using System;

public class Program
{
	public static void Main()
	{
		string numeroStr = "10";
		decimal numero = decimal.Parse(numeroStr);
		Console.WriteLine(numero); // Saída: 10
	}
}
````

> TryParse:

````
using System;

public class Program
{
	public static void Main()
	{
		string numeroStr = "10";
		if (decimal.TryParse(numeroStr, out decimal numero))
		{
			Console.WriteLine($"Valor convertido: {numero}"); // Saída: Valor convertido: 10
		}
	}
}
````

> Convert

````
using System;

public class Program
{
	public static void Main()
	{
		string numeroStr = "10";
		decimal numero = Convert.ToDecimal(numeroStr);
		Console.WriteLine(numero); // Saída: 10
	}
}
````

## Double

O tipo Double representa um número de 64 bits de precisão dupla com valores que variam de `-1.79769313486232` a `1.79769313486232`, bem como zero positivo ou negativo. 

Ele se destina a representar valores extremamente grandes (como distâncias entre planetas ou Galaxias) ou extremamente pequenos (como a massa de molecular de uma substância em quilogramas) e que geralmente são imprecisos (como a distância da terra para outro sistema solar).

### Trabalhando com doubles

Definindo uma variável do tipo decimal:

````
double numero = 1;
````

````
double numero = 2.5;
````

````
var numero = 2.5;
````

#### Conversores (Parse, TryParse, Convert);

> Parse: 

````
using System;

public class Program
{
	public static void Main()
	{
		string numeroStr = "10";
		double numero = double.Parse(numeroStr);
		Console.WriteLine(numero); // Saída: 10
	}
}
````

> TryParse:

````
using System;

public class Program
{
	public static void Main()
	{
		string numeroStr = "10";
		if (double.TryParse(numeroStr, out double numero))
		{
			Console.WriteLine($"Valor convertido: {numero}"); // Saída: Valor convertido: 10
		}
	}
}
````

> Convert

````
using System;

public class Program
{
	public static void Main()
	{
		string numeroStr = "10";
		double numero = Convert.ToDouble(numeroStr);
		Console.WriteLine(numero); // Saída: 10
	}
}
````

## Byte

Byte é um tipo de valor imutável que representa inteiros não assinados com valores que variam de 0 a 255. 

O .NET também inclui um tipo de valor inteiro de 8 bits assinado, SByte , que representa valores que variam de -128 a 127.

O Tipo byte é muito utilizado quando queremos manipular arquivos do sistema, e precisamos ler ou gravar arquivos da memoria do computador.

### Trabalhando com bytes

Definindo uma variável do tipo byte:

````
byte valor = 64;
````

````
byte valor = 255;
````

````
var valor = (byte)25;
````

## DateTime

O tipo DateTime representa datas e horas com valores variando de 00:00:00 (meia-noite), 1º de janeiro de 0001 Anno Domini (era comum) até 11:59:59 P.M., 31 de dezembro, 9999 d.c. (C.E.) no calendário gregoriano.

### Trabalhando com DateTime

Definindo uma variável do tipo DateTime:

````
var data = new DateTime(2008, 5, 1, 8, 30, 52);
````

````
DateTime data = DateTime.Now;
````

````
DateTime data = DateTime.UtcNow;
````

````
DateTime data = DateTime.Today;
````

Existem várias sobrecargas para a impressão de datas em formato de texto, o .Net fornece por padrão, o formato da data usado no computador em que o aplicativo está sendo utilizado, mas esse formato pode ser alterado da forma que desejarmos, como nestes exemplos:

````
using System;

public class Program
{
	public static void Main()
	{
		DateTime data = new DateTime(2000, 1, 1);
		Console.WriteLine(data);  // Saída: 01/01/2000 00:00:00
		Console.WriteLine(data.ToString("dd/MM/yyyy")); // Saída: 01/01/2000
		Console.WriteLine(data.ToString("dd/MM/yyyy HH:mm:ss")); // Saída: 01/01/2000 00:00:00
		Console.WriteLine(data.ToString("dd/MM/yyyy HH:mm:ss.sss")); // Saída: 01/01/2000 00:00:00.00
		Console.WriteLine(data.ToString("MMMM yyyy")); // Saída: January 2000
		Console.WriteLine(data.ToString("MMMM yy")); // Saída: January 00
		Console.WriteLine(data.ToString("dddd, MMMM yyyy")); // Saída: Saturday, January 2000
	}
}
````

## Arrays

Um Array é um conjunto de elementos de um mesmo tipo de dados onde cada elemento do conjunto é acessado pela posição no array que é dada através de um índice (uma sequência de números inteiros).  Um array de uma dimensão é também conhecido como vetor,e , um array de mais de uma dimensão e conhecido como uma matriz.

Um array é uma estrutura de dados que contém uma série de dados ordenados, chamados "elementos". Os elementos são referenciados por número ordinal (índice), primeiro elemento é 0, segundo 1, etc.

 Os elementos podem ser de qualquer tipo, string, char, int, double, etc...

No C#  os arrays possuem o índice com base zero, ou seja, o primeiro elemento do array possui o índice zero (0).

Um array de uma dimensão é declarado informando o tipo de dados do array seguido do nome do array, lembrando que devemos colocar colchetes `[]` depois do tipo do array e não após o seu nome:

````
int[] numeros = {1, 2}; // Cria um array de 2 posições contendo os valores que passamos dentro das chaves
````

````
var numeros = new int[10]; // Cria um array com 10 posições mas nenhum elemento iniciado
````

### Trabalhando com arrays

Para definir os valores de um array que definimos sem nenhum valor, basta atribuir um valor a um índice específico, atribuindo o tipo correto aquele índice:

````
numeros[0] = 1;
numeros[1] = 2;
numeros[2] = 3;
numeros[7] = 4;
numeros[9] = 10;
````

Para acessarmos os valores de um array, seguimos a mesma lógica da atribuição de valor, onde usamos o índice que desejamos acessar para ter acesso ao valor que está atribuído a aquela poição do array:

````
Console.WriteLine(numeros[0]); // Valor: 1
Console.WriteLine(numeros[9]); // Valor: 10
Console.WriteLine(numeros[2]); // Valor: 3
````

Mas acessar todos os elementos de um array manualmente é quase impossível, sendo que podemos ter arrays gigantes com muitos elementos e não queremos ter que escrever uma linha de código para acessar cada um desses valores, pra isso usamos os laços de repetição:

> For

````
using System;

public class Program
{
	public static void Main()
	{
		string[] carros = {"Volvo", "BMW", "Ford", "Mazda"};
		for (int i = 0; i < carros.Length; i++)
		{
			Console.WriteLine(carros[i]);
		}
	}
}
````

> Foreach

````
using System;

public class Program
{
	public static void Main()
	{
		string[] carros = {"Volvo", "BMW", "Ford", "Mazda"};
		foreach(var carro in carros)
		{
			Console.WriteLine(carro);
		}
	}
}
````

### Arrays de duas dimensões

Para um array de mais de uma dimensão a sintaxe usada para instanciá-lo pode ser:

````
string[,] nomes = new string[5,4]; // Declara um array bidimensional com 5 linhas e 4 colunas
````

````
int [,] matriz = new int [3,4] {
   {0, 1, 2, 3} ,   /*  inicia a linha indexada por 0 */
   {4, 5, 6, 7} ,   /*  inicia a linha indexada por 1 */
   {8, 9, 10, 11}   /*  inicia a linha indexada por 2 */
};
````

Para o acesso de dados ou atribuição de valores em um array bidimencional, seguimos a mesma lógica de um array comum, porém agora sempre temos que prestar atenção na linha e coluna que queremos referenciar:

````
using System;

public class Program
{
	public static void Main()
	{
		int[, ] a = new int[5, 2]{{0, 0}, {1, 2}, {2, 4}, {3, 6}, {4, 8}};
		for (int i = 0; i < 5; i++)
		{
			for (int j = 0; j < 2; j++)
			{
				Console.WriteLine("a[{0},{1}] = {2}", i, j, a[i, j]);
			}
		}

        /*
        Saída:
        
        a[0,0] = 0
        a[0,1] = 0
        a[1,0] = 1
        a[1,1] = 2
        a[2,0] = 2
        a[2,1] = 4
        a[3,0] = 3
        a[3,1] = 6
        a[4,0] = 4
        a[4,1] = 8
        */
	}
}
````

# Null

O C# é uma das linguagens de programação que oferece suporte a tipos `nullables`, ou seja, de um modo prático quer dizer que conseguimos iniciar objetos e variáveis e não atribuir valor algum a eles. Basicamente o que fazemos é reservar um espaço na memória que está apontando temporariamente para nenhum valor.

Essa implementação tem dois lados, um que pode facilitar nossa vida, e outro que pode atrapalhar. Podemos iniciar variáveis como:

````
int? x = null;
````

O que pode ser bom, se temos a necessidade de iniciar uma variável `x` sem valor temporariamente por algum motivo. Porém, se em algum ponto do sistema tentarmos fazer alguma operação com essa variável `x`, sem ainda ter atribuído um valor a ela, temos a temida `NullReferenceException`, que indica que tentamos acessar um valor na memória que não existe.

Isso pode causar muitos problemas, então temos que prestar muita atenção em como manipulamos os dados para não caírmos nessa falha.

No C#, basicamente todos os tipos podem ser nullables, apenas o identificando-os com o caracter `?` depois da declaração de seu tipo.

````
int? x = null;

double? x = null;

DateTime? x = null;

string? x = null;
````

> Todos os objetos que implementam esse comportamento nullable, tem seu valor padrão como `null`, que pode ser diferente do seu tipo "não nullable", e implementam a função `HasValue` e a propriedade `Value`, para checagem e uso do valor respectivamente.

# Tipos de valor

Tipos de valor e tipos de referência são as duas principais categorias de tipos do C#.

Uma variável de um tipo de valor, contém uma instância do tipo. Isso é diferente de uma variável de um tipo de referência, que contém uma referência a uma instância do tipo. 

Ou seja, simplificando, cada variável do tipo de valor contém sua própria referência exclusiva, e mesmo quando copiada, não compartilha essa referência, ficando a cargo do CLR criar um novo local de armazenamento para a nova variável.

Por padrão, na atribuição, passando um argumento para um método e retornando um resultado de método, valores de variáveis são copiados. No caso de variáveis de tipo de valor, as
instâncias de tipo correspondentes são copiadas. O exemplo a seguir demonstra esse comportamento:


````
using System;

public struct MutablePoint
{
	public int X;
	public int Y;
	public MutablePoint(int x, int y) => (X, Y) = (x, y);
	public override string ToString() => $"({X}, {Y})";
}

public class Program
{
	public static void Main()
	{
		var p1 = new MutablePoint(1, 2);
		var p2 = p1;
		p2.Y = 200;
		Console.WriteLine($"{nameof(p1)} after {nameof(p2)} is modified: {p1}");
		Console.WriteLine($"{nameof(p2)}: {p2}");
		MutateAndDisplay(p2);
		Console.WriteLine($"{nameof(p2)} after passing to a method: {p2}");
	}

	private static void MutateAndDisplay(MutablePoint p)
	{
		p.X = 100;
		Console.WriteLine($"Point mutated in a method: {p}");
	}
}
// Expected output:
// p1 after p2 is modified: (1, 2)
// p2: (1, 200)
// Point mutated in a method: (100, 200)
// p2 after passing to a method: (1, 200)

````

# Tipos de referência

Variáveis de tipos de referência armazenam referências em seus dados (objetos) enquanto que variáveis de tipos de valor contém diretamente seus dados. Com tipos de referência, **duas variáveis podem fazer referência ao mesmo objeto**, portanto, operações em uma variável
podem afetar o objeto referenciado pela outra variável. Com tipos de valor, cada variável tem sua própria cópia dos dados e as operações em uma variável não podem afetar a outra.

Ou seja, simplificando, um tipo de referência na verdade está apontada para um endereço de memória que contém o seu valor de fato, quando copiamos uma variável deste tipo, estamos copiando este endereço, e não seu valor, sendo assim, quando alteramos os valores de uma dessas copias, o valor é alterado nas duas instâncias, já que elas apontam para o mesmo endereço de memória.

# Palavras-chave

As palavras-chave são identificadores reservados predefinidos com significados especiais para o compilador. Elas não podem ser usadas como identificadores em seu programa, a não ser que incluam @ como prefixo. Por exemplo, @if é um identificador válido, mas if não é porque if é uma palavra-chave.

Abaixo está uma lista com algumas palavras-chaves mais conhecidas do C#:

|          |           |            |           |
|----------|-----------|------------|-----------|
| abstract | namespace | new        | struct    |
| as       | event     | null       | switch    |
| base     | explicit  | object     | this      |
| bool     | extern    | operator   | throw     |
| break    | false     | out        | true      |
| byte     | finally   | override   | try       |
| case     | fixed     | params     | typeof    |
| catch    | float     | private    | uint      |
| char     | for       | protected  | ulong     |
| checked  | foreach   | public     | unchecked |
| class    | goto      | readonly   | unsafe    |
| const    | if        | ref        | ushort    |
| continue | implicit  | return     | using     |
| decimal  | in        | sbyte      | virtual   |
| default  | int       | sealed     | void      |
| delegate | interface | short      | volatile  |
| do       | internal  | sizeof     | while     |
| double   | is        | stackalloc |           |
| else     | lock      | static     |           |
| enum     | long      | string     |           |

---

# Funções

Um método, ou uma função, é um bloco de código que contém uma série de instruções. 
Um programa faz com que as instruções sejam executadas chamando o método e especificando os argumentos de método necessários. No C#, todas as instruções executadas são realizadas no contexto de um método.

O método `Main` é o ponto deentrada para cada aplicativo C# e échamado pelo Common Language Runtime (CLR) quando o programa é iniciado.

### Assinaturas de método

Os métodos são declarados em uma classe, struct ou interface especificando o nível de acesso como public ou private, modificadores opcionais, como abstract ou sealed, o tipo de valor de retorno, o nome do método e seus parâmetros. Juntas, essas partes são a assinatura do método.

````
abstract class Moto
{
	// Qualquer um tem acesso
	public void Ligar()
	{
	}

	// Somente classes derivadas de Moto tem acesso
	protected void Abastecer(int litros)
	{
	}

	// Classes derivadas tem acesso e podem sobrecarregar este método
	public virtual int Andar(int distancia, int velocidade)
	{
		return 1;
	}

	// Classes derivadas devem implementar este método
	public abstract double VelocidadeMaxima();
}
````
### Acesso de método

Chamar um método em um objeto é como acessar um campo. Após o nome do objeto, adicione um ponto final, o nome do método e parênteses. Os argumentos são listados dentro dos parênteses e são separados por vírgulas. 

Os métodos da classe Moto podem, portanto, ser chamados como no exemplo a seguir:

````
using System;

class MotoTest : Moto
{
	public override double VelocidadeMaxima()
	{
		return 108.4;
	}
}
					
public class Program
{
	public static void Main()
	{
		MotoTest moto = new MotoTest();
		moto.Ligar();
		moto.Abastecer(15);
		moto.Andar(5, 20);
		double speed = moto.VelocidadeMaxima();
		Console.WriteLine("A velocidade máxima é: {0}", speed);
	}
}

````

### Parâmetros do método vs. argumentos

A definição do método especifica os nomes etipos de quaisquer parâmetros obrigatórios. Quando o código de chamada chama o método, ele fornece valores concretos, chamados argumentos, para cada parâmetro. Os argumentos devem ser compatíveis com o tipo de parâmetro, mas o nome do argumento (se houver) usado no código de chamada não precisa ser o mesmo que o parâmetro nomeado definido no método.

### Passando por referência vs. passando por valor

Por padrão, quando uma instância de um tipo de valor é passada para um método, sua cópia é passada em vez da própria instância. Portanto, as alterações no argumento não têm efeito sobre a instância original no método de chamada. Para passar uma instância de tipo de valor por referência, use a palavra-chave `ref`.

#### Passando por referência

Quando um objeto detipo dereferência é passado para um método, uma referência ao objeto é passada. Ou seja, o método recebe não o objeto em si, mas um argumento que indica o local do objeto. Se você alterar um membro do objeto usando essa referência, a alteração será refletida no argumento no método de chamada, ainda que você passe o objeto por valor.

````
using System;

public class Program
{
	public static void Method(ref int refArgument)
	{
		refArgument = refArgument + 44;
	}
	
	public static void Main()
	{
		int number = 1;
		Method(ref number);
		Console.WriteLine(number); // Saída: 45
	}	
}
````

#### Passando por valor

Quando usamos um tipo de valor, é passada para um método, sua cópia é passada em vez da própria instância. Portanto, as alterações no argumento não têm efeito sobre a instância original no método de chamada.

````
using System;

public class Program
{
	public static void Method(int arg)
	{
		arg = arg + 44;
	}
	
	public static void Main()
	{
		int number = 1;
		Method(number);
		Console.WriteLine(number); // Saída: 1
	}	
}
````

### Parâmetros de entrada (in)

A palavra-chave `in` faz com que os argumentos sejam passados por referência, mas garante que o argumento não seja modificado. 

Ela torna o parâmetro um alias para o argumento, que deve ser uma variável. Em outras palavras, qualquer operação no parâmetro é feita no argumento. É como as palavras-chave `ref` ou `out`, exceto que os argumentos `in` não podem ser modificados pelo método chamado.

````
using System;

public class Program
{
	public static void Method(in int arg)
	{
        // Se descomentarmos essa linha, vemos o erro "Cannot assign to variable 'in int' because it is a readonly variable"
        // Porque estamos tentando alterar o valor de uma parâmetro de entrada
		// arg = arg + 44;
	}
	
	public static void Main()
	{
		int number = 1;
		Method(number);
		Console.WriteLine(number); // Saída: 1
	}	
}
````

### Parâmetros de saída (out)

A palavra-chave `out` faz com que os argumentos sejam passados por referência. 

Ela torna o parâmetro um alias para o argumento, que deve ser uma variável. Em outras palavras, qualquer operação no parâmetro é feita no argumento. É como a palavra-chave `ref`, exceto pelo fato de que `ref` requer que a variável seja inicializada antes de ser passada. 

````
using System;

public class Program
{
	public static void OutArgExample(out int number)
	{
		number = 44;
	}

	public static void Main()
	{
		int initializeInMethod;
		OutArgExample(out initializeInMethod);
		Console.WriteLine(initializeInMethod); // Saída: 44
	}
}
````

---

# Orientação a objetos

O desenvolvimento de software é extremamente amplo. Nesse mercado, existem diversas linguagens de programação, que seguem diferentes paradigmas. Um desses paradigmas é a Orientação a Objetos, que atualmente é o mais difundido entre todos. Isso acontece porque se trata de um padrão que tem evoluído muito, principalmente em questões voltadas para segurança e reaproveitamento de código, o que é muito importante no desenvolvimento de qualquer aplicação moderna.
 
> **O que é um paradigma de programação?**  
Um paradigma pode ser entendido como a forma com a qual se decide resolver determinado problema por meio da programação de computadores. Nesse sentido, temos alguns paradigmas possíveis que eventualmente podem ser usados mais de um (caso a linguagem escolhida ofereça suporte).

O paradigma da POO (Programação Orientada a Objetos) é um modelo de análise, projeto e programação baseado na aproximação entre o mundo real e o mundo virtual, através da criação e interação entre objetos, atributos, códigos, métodos, entre outros.

A programação orientada a objetos tem o propósito principal de aproximar o mundo lógico da programação e o mundo em que vivemos. À vista disso, ela parte do princípio de que tudo é objeto — isso mesmo, tudo o que existe são os objetos.

### Classes

Uma classe é um gabarito para a definição de objetos. Através da definição de uma classe, descreve-se que propriedades ou atributos o objeto terá.

Uma classe mantém dois elementos importantes: `estrutura e comportamento`.

* Uma estrutura representa os atributos que descrevem a classe.
* Um comportamento representa os serviços que a classe suporta.

Imagine que você queira representar uma pessoa como um objeto de um sistema, olhando para essas duas palavras `estrutura e comportamento`, como poderíamos fazer essa representação?

> Estrutura

Como podemos pensar na `estrutura` para que possamos representar uma pessoa, dentro de um sistema de computador?

Bom, primeiro teríamos que saber quais tipos de `dados` que nosso sistema precisa para poder representar uma pessoa do jeito mais simples e coeso o possível. Poderíamos falar que um objeto de pessoa tem dois braços, duas pernas, duas mãos com cinco dedos em cada uma, cabelo, nariz, boca, orelha e assim por diante... Mas qual a utilidade desses dados no nosso sistema?

Digamos que nosso sistema é um sistema de cadastro para promoção de uma padaria, quais dados precisamos para representar cada pessoa nesse cadastro?

Agora já temos uma ideia melhor de onde começar, e do que precisamos. Vamos representar uma pessoa com os seguintes dados: **Nome**, **Sobrenome**, **Idade**, **CPF** e **Telefone**.

Então a `estrutura` da nossa classe ja foi definida. Vamos pensar no seu `comportamento`.

> Comportamento

No contexto que definimos, um cadastro para sorteio de uma padaria, quais comportamentos uma pessoa assume?

Bom, podemos dizer que ela **realiza o cadastro no sorteio**, e pode **verificar o resultado** no dia do mesmo.

Então definimos os dois comportamentos da nossa classe. E podemos representar ela desse jeito:

![diagrama-1](./pessoa-2.png)

## Herança

O reuso de código é uma das grandes vantagens da programação orientada a objetos. Muito disso se dá por uma questão que é conhecida como herança. Essa característica otimiza a produção da aplicação em tempo e linhas de código.

A herança é um mecanismo que permite que características comuns a diversas classes sejam agrupadas em uma classe base, ou superclasse. A partir de uma classe base, outras classes podem ser especificadas. Cada classe derivada ou subclasse apresenta as características (estrutura e métodos) da classe base e acrescenta a elas o que for definido de particularidade para ela.

Imaginamos a classe pessoa que descrevemos, nesse momento, somente definimos uma pessoa como um cliente/participante do sorteio, porém, podemos pensar também que existe um tipo de pessoa que está gerindo esse sorteio, como um funcionario da padaria.

Porém, esse funcionário tem uma estrutura muito parecida com um cliente da padaria, eles compartilham sua estrutura `base`. Para não termos duas definição de classe `pessoa`, uma para o cliente, e outra para o funcionário, usamos da herança para definir uma classe base com os dados compartilhados entre esses dois objetos, e implementamos, para cada tipo de pessoa diferente um novo tipo, que herda dessa classe base:

![diagrama-2](./pessoa-3.png)

Veja que a classe base `pessoa` passou a ter somente os dados que os tipos `funcionario` e `cliente` compartilham, ficando a cargo de cada uma agora, implementar os dados pertinentes ao seu tipo, como o cargo do funcionário, ou o telefone do cliente.

## Encapsulamento

O encapsulamento é uma das principais técnicas que define a programação orientada a objetos. Se trata de um dos elementos que adicionam segurança à aplicação em uma programação orientada a objetos pelo fato de esconder as propriedades, criando uma espécie de caixa preta.

O encapsulamento ele define que cada objeto contém todos os detalhes de implementação necessários sobre como ele funciona e oculta os detalhes internos sobre como ele executa os serviços.

No exemplo das nossas classes de pessoa, o `comportamento` de cada um está encapsulado dentro de seus métodos e propriedades específicas, podemos usar um outro exemplo para exemplificar:

![diagrama-3](./carro-1.png)

No diagrama temos definida a classe base `Carro`, e duas outras que fazem herança da mesma, `BMW` e `Mercedes`. 

Note que dentro da classe base, foi definida uma função, ou comportamento, `Acelerar`, que é comum para todos os carros. Mas todos os carros fazem isso de um jeito diferente, um carro pode ter um acelerador elétrico, o outro a cabo e assim por diante, mas usando corretamente o encapsulamento todos os carros implementam esse comportamento, sem se preocupar com o que o outro objeto está fazendo, cada objeto que implementa essa classe base encapsula a função de acelerar, e pela perspectiva de um carro, todos eles aceleram, sem necessariamente saber como o processo é desenvolvido por baixo dos panos.

## Polimorfismo

Outro ponto essencial na programação orientada a objetos é o chamado polimorfismo. Na natureza, vemos animais que são capazes de alterar sua forma conforme a necessidade, e é dessa ideia que vem o polimorfismo na orientação a objetos. Como sabemos, os objetos filhos herdam as características e ações de seus “ancestrais”. Entretanto, em alguns casos, é necessário que as ações para um mesmo método seja diferente. Em outras palavras, o polimorfismo consiste na alteração do funcionamento interno de um método herdado de um objeto pai.

Como um exemplo, podemos definir um objeto base `Animal`, e algumas outras classes que herdam dessa classe.

A classe `Animal` tem um comportamento que se chama `Falar`, e toda classe que herda desta deve implementar essa função conforme necessário:

![diagrama-4](./animal-1.png)

Podemos considerar que quando um objeto da classe `Cachorro` implementar a função `Falar`, será diferente da implementação da classe `Gato`.

## Abstratação

Também chamada de interface ou template. Muitos simplificam sua explicação como sendo uma espécie de mistura de encapsulamento e polimorfismo. A ideia principal é representar um objeto de forma abstrata, que seja obrigatoriamente herdado por outras classes.

Como nos exemplos anteriores, usamos a abstração para criar um `contrato` na classe base, e obrigamos as classes que herdam dela a implementa-los, como vimos na função `Falar` do animal, ou `Acelerar` do carro.

---

# Listas

Para facilitar nossa vida o C# implementou um sistemas de listas mais avançados do que os arrays e matrizes que já vimos. Foram desenvolvidadas várias interfaces, que tem como base a `IEnumerable<T>`, e essas oferecem várias vantagens para nós programadores e torna nossa vida mais prática, como o uso do `LINQ`, métodos de extensões, gerenciamento de memória entre outras coisas...

Uma lista, ao contrário de um array, tem o tamanho dinâmico, não é necessário definir o tamanho de uma lista no momento da sua criação, automaticamente, conforme necessidade, é alocado mais espaço na memória para comportar nosso objeto.

Existem vários tipos de listas por padrão no C#, e isso confunde um pouco qual tipo de lista escolher para cada situação, vamos falar das mais comuns:

> IList\<T>

É a mais comum, oferece mais métodos e liberdade para realizar operações na lista em troca de uma performance razoável.

> IEnumerable\<T>

Das interfaces é a mais comum, como já dito, é a interface base para todas as listas, então é bastante usada como retorno de funções, onde o chamador da função pode fazer a conversão da mesma para outro tipo de lista como o `List\<T>`.

> IReadOnlyCollection\<T>

É muito usada quando precisamos iniciar uma lista no momento da criação de um objeto por exemplo, e não queremos que esses dados sejam modificados posteriormente, é uma lista somente leitura.

> IDictionary\<T>

É também uma das mais conhecidas, quando precisamos de uma lista de chave-valor, onde a chave não pode se repetir.

### Trabalhando com listas

Para instanciarmos uma lista, temos que usar o namespace `System.Collections.Generic`, e podemos declará-la das seguintes maneiras:

````
var list = new List<string>() {"a", "b", "c", "d"};
````

````
List<string> list = new List<string>() {"a", "b", "c", "d"};
````

````
List<string> list = new List<string>();
````

````
List<string> list = null;
````

> Diferente dos arrays, não precisamos definir o tamanho da lista no momento da sua criação.

Adicionando valores em uma lista:

````
using System;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var list = new List<char>() {'a', 'b', 'c', 'd'};

        list.Add('e');
        list.Add('f');
        list.Add('g');
		
		list.ForEach(x => {
			Console.WriteLine(x);
		});
	}
}
````

Iterando os valores de uma lista:

````
using System;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var list = new List<char>() {'a', 'b', 'c', 'd'};
		
        // Podemos usar essa sintaxe do foreach        
        foreach(var chr in list)
		{
			Console.WriteLine(chr);
		}

        // Ou essa outra
        list.ForEach(x => {
			Console.WriteLine(x);
		});

        // Acessando o valor como num array usando colchetes e o index
        for (int i = 0; i < list.Count; i++)
		{
			Console.WriteLine(list[i]);
		}
	}
}
````

Removendo valores de uma lista:

````
using System;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var list = new List<char>() {'a', 'b', 'c', 'd'};

       list.Remove('a');
		
		list.ForEach(x => {
			Console.WriteLine(x);
		});
	}
}
````

## LINQ

Como já foi mencionado, junto com as listas, o C# oferece um namespace `System.Linq` onde ficam as operações do `LINQ` ou `Language-Integrated Query`, que permitem uma padronização de como as listas são manipuladas no C#. 

O `LINQ` oferece vários métodos de extensão que permitem a manipulação de listas de um jeito prático, assim também como uma sintaxe própria, semelhante ao SQL que também pode ser usada nos aplicativos do .Net.

Vamos ver os métodos mais usados da biblioteca:

> Where

O método `Where` faz a busca na lista baseado na expressão que é passada por parâmetro:

````
using System;
using System.Linq;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var list = new List<char>() {'a', 'b', 'c', 'd', 'a'};
		var chrs = list.Where(c => c == 'a');
		
		foreach(var chr in chrs)
		{
			Console.WriteLine(chr);
		}
	}
}
````

> Any

O método `Any` verrifica se existe alguma ocorrência na lista baseado na expressão passada por parâmetro e retorna True caso exista ou False caso não:

````
using System;
using System.Linq;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var list = new List<char>() {'a', 'b', 'c', 'd', 'a'};
		Console.WriteLine(list.Any(c => c == 'a'));
	}
}
````

> First

O método `First` busca o primeiro elemento da lista, ou o primeiro elemento a satisfazer a expressão passada por parâmetro:

````
using System;
using System.Linq;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var list = new List<char>() {'a', 'b', 'c', 'd', 'a'};
		Console.WriteLine(list.First(c => c == 'a'));
	}
}
````

> SingleOrDefault;

O método `SingleOrDefault` busca o primeiro e único elemento da lista ou o null caso vazio, ou o primeiro elemento a satisfazer a expressão passada por parâmetro, caso haja mais de um elemento que satisfaça a mesma condição, uma excessão será lançada:

````
using System;
using System.Linq;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var list = new List<char>() {'a', 'b', 'c', 'd'};
		Console.WriteLine(list.SingleOrDefault(c => c == 'a'));
	}
}
````

> FirstOrDefault

O método `FirstOrDefault` busca o primeiro elemento da lista ou o null caso vazio, ou o primeiro elemento a satisfazer a expressão passada por parâmetro, ao contrário do `SingleOrDefault`, caso haja mais de um elemento que satisfaça a mesma condição, nenhuma excessão será lançada:

````
using System;
using System.Linq;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var list = new List<char>() {'a', 'b', 'c', 'd', 'a'};
		Console.WriteLine(list.FirstOrDefault(c => c == 'a'));
	}
}
````

> Count

O método `Count` retorna o número total de elementos da lista, ou o número total de elementos da lista a satisfazer a expressão passada por parâmetro:

````
using System;
using System.Linq;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var list = new List<char>() {'a', 'b', 'c', 'd', 'a'};
		Console.WriteLine(list.Count(c => c == 'a'));
	}
}
````

> GroupBy

O método `GroupBy` retorna uma nova lista onde os valores são agrupados pelos valores que foram passados por parametro:

````
using System;
using System.Linq;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var list = new List<char>() {'a', 'b', 'c', 'd'};
		Console.WriteLine(list.GroupBy(c => c));
	}
}
````

> Select

O método `Select` retorna uma nova lista onde os valores são resultado das propriedades ou objeto anônimo passado por parametro:

````
using System;
using System.Linq;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var list = new List<char>() {'a', 'b', 'c', 'd'};
		Console.WriteLine(list.Select(c => new {  NovaString = c.ToString() } ).First());
	}
}
````

> Contains

O método `Contains` verifica se uma lista está contida dentro de outra, ou contém um elemento específico, e retorna True caso sim ou False caso não:

````
using System;
using System.Linq;
using System.Collections.Generic;

public class Program
{
	public static void Main()
	{
		var list = new List<char>() {'a', 'b', 'c', 'd'};
		Console.WriteLine(list.Contains('a'));
	}
}
````
