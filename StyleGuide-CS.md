# Guia de Estilos do C\# #
Nesse guia reunimos os padrões de estilos recomendados pela Caeno para escrita de código na linguagem C#. O objetivo é garantir que o código seja o mais organizado e legível possível, bem como permitir que os desenvolvedores se encontrem facilmente dentro de novos projetos.

Seguimos os principios de concisão, legibilidade e simplicidade.

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