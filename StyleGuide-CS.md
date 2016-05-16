# Guia de Estilos do C\# #
Nesse guia reunimos os padrões de estilos recomendados pela Caeno para escrita de código na linguagem C#. O objetivo é garantir que o código seja o mais organizado e legível possível, bem como permitir que os desenvolvedores se encontrem facilmente dentro de novos projetos.

Seguimos os principios de concisão, legibilidade e simplicidade.

># Conversa Homem/Máquina
As linguagens de programação são a forma que criamos para nos comunicarmos com nossos computadores e não receberam esse nome por acaso! Tal como as linguas humanas faladas ou escritas elas empregam regras de ortografia e sintaxe, que devem ser estritamente seguidas caso desejemos nos fazer claro para o nosso interlocutor: o computador! 

>Mas nunca podemos nos esquecer que essa conversa não é um monólogo, mas sim um diálogo que acontece entre você, o computador e todos os outros seres humanos que participam daquele projeto.

>Quando pessoas participam de um intercambio é muito comum que elas encontrem no outro país pessoas de diversas regiões e culturas diferentes que para se comunicar fazem uso de uma língua comum (em geral o inglês). Nem todos são proficientes naquele idioma mas todos se esforçam para manter um bom nível de contato e isso só é possível graças aos padrões que essas línguas foram integrando ao longo do tempo.  

>Um bom programador não encara sua linguagem de programação como um simples instrumento, ele tem respeito pelas estruturas e boas práticas daquele língua, tal como um academico pelo idioma que emprega na escrita de um artigo científico. Escreva seu código como se estivesse escrevendo uma monografia e não como se estivesse conversando no WhatsApp. Seus pares agradecerão.

>Linguagens de programação são tão vivas quanto os idiomas falados, mudando frequentemente, empregando novas gírias e sotaques que surgem nos diversos meios aonde são utilizadas. Esteja sempre atento ao que acontece com o seu meio e aberto as novidades, pois isso tenderá sempre a tornar seu trabalho mais produtivo. Por esse motivo esse documento não tem como objetivo estabelecer padrões rígidos, mas sim indicar as melhoras práticas na escrita de programas de computador, tal como a Metodologia Científica procura estabelecer padrões que facilitam a comunicação no meio acadêmico. O objetivo não é burocratizar e sim facilitar.

>Empenhe-se no estudo e aplicação dessas sugestões e observe o impacto disso no trabalho do seu dia-a-dia.

Consulte o [glossário](Glossary.md) para termos e convenções comuns a todas as linguagens. 

## Uso da Língua 
Ao programarmos devemos criar símbolos e identificadores para os elementos do código, bem como documentar ou incluir comentários para explicar trechos com uma lógica mais intrincada.

Devemos **sempre** utilizar a **Língua Inglesa** com o objetivo de tornar o nosso código acessível a maior quantidade de programadores. Hoje em dia nunca sabemos se pessoas de outros países ou cultura possam chegar a integrar nossos projetos e precisamos estar preparados para isso. Num cenário de código aberta isso também é fundamental para que um projeto possa ter o maior número de colaboradores possível.

Entendemos que nem todos os programadores tem familiaridade ou facilidade com inglês. Nessas situações encorajamos que seus colegas mais experientes sejam consultados ou que um tradutor como o Google ou Bing sejam utilizados. 

## Nomes
Use nomes descritivos e significativos. Evite nomes genéricos ou que não remetem de maneira alguma ao própsito de um tipo ou variável. Os ambientes de desenvolvimento (IDE's) modernos empregam recursos como Intellisense ou Autocomplete que ajudam com nomes grandes, por isso não se preocupe em utilizar nomes grandes caso eles sejam significativos ao seu propósito.

Classes, estruturas, enumerações e outras declarações gerais de tipos devem utilizar o estilo *Pascal Case*. O mesmo vale para declarações de nomes de propriedades ou variáveis:

```csharp
public class Vehicle {
    
    public int Wheels { get; set; }
    
    public void MoveForward() {
        // Code to move forward...
    }     
    
}
```

Argumentos de métodos e variáveis declaradas no corpo dos métodos ou lambdas devem usar o estilo *Camel Case*:

```csharp
public int Calculate(int firstNumber, int secondNumber) {
    int theResult = firstNumber + secondNumber;
    return theResult;
}
```

Os campos privados de um classe ou struct devem seguir o estilo *Camel Case* prefixando com um *_* (underscore). Isso permite distingui-los facilmente de argumentos e variáveis quando o código for escrito.

*(TODO: incluir snippet de exemplo)*

Interfaces devem seguir o estilo *Pascal Case* e ter seu nome sempre prefixado com a letra **I** maiúscula, de forma que as duas primeiras letras serão sempre maiúsculas:

```csharp
public interface IRepository<T> {
    
    void Add(T obj);
    
    T Get(int id);
     
    // ...
      
}
```

Essa convenção permite nos dintinguir rapidamente se estamos trabalhando com uma classe ou uma interface. Se a primeira letra do nome de uma interface começar com *I* repita a letra:

```csharp
public interface IIdentity {
 
    int GetId();
    
}
```

Constantes e campos somente leitura devem usar a notação *Upper Case*:

```csharp
const int MAX_PICTURES = 5;
const string PICTURES_PATH_KEY = "picturesPath";
```

## Documentação


## Organização do Código


## Tabulação


## Declarações de Blocos


## Inferência de Tipos


## Classes ou Estruturas


## Uso do *this*


## Lambdas