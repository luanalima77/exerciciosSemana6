# Instruções
- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 8 questões objetivas assinalando a alternativa correta e **justificando sua resposta.**
- Resolva as 2 questões dissertativas escrevendo no próprio arquivo .md
- Lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com o uso de ChatGPT (e similares), pois entregar algo só para ganhar nota não fará você aprender. Não seja dependente da máquina!
- Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
a) A saída será undefined seguido de erro 

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

<h2>MINHA RESPOSTA DA 1): A) </h2>
<p> JUSTIFICATIVA: O primeiro console.log está tentando acessar uma variável do tipo var, que é movida para o topo devido ao seu escopo global, porém ela ainda não foi definida no momento em que foi chamada (por isso o undefined). Já o segundo console.log tenta acessar uma variável do tipo let, que não permite acesso à variável antes de sua declaração (por isso o erro no código).</p> <br> <br>

**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

<h2>MINHA RESPOSTA DA 2): A) </h2>
<p> JUSTIFICATIVA: O código fornecido no enunciado verifica se a é um valor truthy (qualquer valor diferente de falsy, como visto nos autoestudos) ou se b é igual a 0. No entanto, o intuito da proposta é verificar se qualquer uma das variáveis (a ou b) é exatamente igual a 0. Logo, com o código da letra a), é possível fazer essa verificação para a e b, retornando “Erro: número inválido” se qualquer uma delas for igual a 0.
</p> <br> <br>

______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

b) O código imprime 200.

c) O código imprime 50.

d) O código gera um erro.

<h2>MINHA RESPOSTA DA 3): B) </h2>
<p> JUSTIFICATIVA: O código do enunciado (quando for executado) vai retornar 200. Ele executa a função calcularPreco passando “eletrônico” como argumento, entrando no case “eletrônico” e fazendo a variável preço receber 1000. Porém, como não há um break nesse case, o próximo case é executado (“vestuário”). No case “vestuário”, é atribuído 200 à variável preço e aí sim há um break, que interrompe o switch. Por isso, a saída no console vai ser 200.</p> <br> <br>

______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

d) 24

<h2>MINHA RESPOSTA DA 4): D) </h2>
<p> JUSTIFICATIVA: A partir do código fornecido no enunciado, é significativo pontuar que nele há 3 métodos:  map, filter e reduce. O map está fazendo com que os elementos do array numeros sejam multiplicados por dois, ou seja, realiza seu dobro: [2, 4, 6, 8, 10]. Assim que isso ocorre, o filter filtra os elementos maiores que 5 no array obtido (no caso 6, 8 e 10). Nesse sentido, o método reduce soma todos os elementos do array, começando a soma pelo número 0. Por conseguinte, a saída no console será 24. </p> <br> <br>

______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

c) ["banana", "abacaxi", "manga", "laranja"]

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

<h2>MINHA RESPOSTA DA 5): C) </h2>
<p> JUSTIFICATIVA: A lista que possui as frutas está passando pelo método splice, que modifica itens de uma lista, podendo colocar elementos no lugar de outros. Segundo o código do enunciado, a troca de elementos começa na posição 1 do array e ela acontece em dois elementos (os de posição 1 e 2, ou seja, "maçã" e "uva"), sendo colocados no lugar deles "abacaxi" e "manga". Então, é possível concluir que o array retornado será ["banana", "abacaxi", "manga", "laranja"].</p> <br> <br>

______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.

<h2>MINHA RESPOSTA DA 6): A) </h2>
<p> JUSTIFICATIVA: a afirmação I está certa porque herança é justamente a capacidade de uma classe herdar métodos e propriedades de outra classe, o que proporciona reutilização de código. Já a afirmação II está correta porque extends é justamente a palavra reservada para uma classe herdar de outra em JavaScript, ou seja, sem ela não é possível aplicar herança nessa linguagem de programação. Por fim, a segunda afirmação justifica a primeira porque, com mencionado anteriormente, extends é o que permite que uma classe herde de outras em JavaScript. Portanto, essas duas afirmações são complementares.</p> <br> <br>

______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

a) I e II são verdadeiras.

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

<h2>MINHA RESPOSTA DA 7): A)</h2>
<p> JUSTIFICATIVA: A afirmação I está certa porque a classe Funcionario, de fato, herda da classe Pessoa, por meio de extends, podendo acessar os atributos nome e idade por meio do método super(). Já a afirmação II está correta, uma vez que a sobrescrita do método apresentar() na classe Funcionario é, realmente, realizada, mostrando o atributo de salário. No entanto, esse método também mostra o nome e a idade, que, como mencionado anteriormente, são atributos herdados da classe Pessoa por meio do super(). Por fim, a III está completamente incorreta, já que o JavaScript suporta sim herança de classes.</p> <br> <br>


______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

b) A asserção é verdadeira e a razão é falsa.

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

<h2>MINHA RESPOSTA DA 8): B)</h2>
<p> JUSTIFICATIVA: a asserção está correta, já que a própria palavra "polimorfismo" indica diferentes formas. Nesse caso, seriam diferentes formas de objetos de diferentes tipos responderem à mesma mensagem (como o próprio enunciado diz). Já a razão está errada, uma vez que o JavaScript não suporta sobrecarga de métodos (em que há métodos com o mesmo nome, porém com parâmetros diferentes). No JavaScript é aplicada a sobrescrita de métodos, em que os métodos da classe que herda redefinem os da classe pai (que promove a herança), mantendo o mesmo nome, por exemplo.</p> <br> <br>
______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```

<h2>MINHA RESPOSTA DA 9</h2>

```javascript
function somaArray(numeros) {
    //1) A variável soma não havia sido inicializada corretamente, pois estava sem palavra reservada para definir o tipo da variável. 
    //Para soma não ficar indefinida, inicializei ela com 0.
    var soma = 0;

    //2) Assim como na variável soma, a varíavel i (dentro do for) não havia sido inicializada corretamente, já que estava sem palavra reservada para definir o tipo da variável. 

    //3) O método para acessar o tamanho de um array não é size, mas sim length.
    for (let i = 0; i < numeros.length; i++) {
        soma += 2 * numeros[i]; //4) Adicionei o operador += para que o novo valor seja somado ao que já foi adicionado anteriormente.
    }

    //Retornando a soma.
    return soma;
}

//Resultado: 20.
console.log(somaArray([1, 2, 3, 4]));
```

______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.

<h2>MINHA RESPOSTA DA 10</h2>
<p> Nesse cenário, a herança faz com que a classe Livro receba atributos e métodos da classe Produto (o nome, o preço e o método para calcular os descontos), que são comuns a ambas as classes, o que é positivo em termos de reutilização de código. Além disso, Livro não deixa de ser uma subclasse de Produto, afinal um livro é um produto, porém com algumas especificações. Quando eu fui fazer o código, eu coloquei o desconto no método construtor: deixei 0.1 (10%) em Produto e 0.2 (20%) em Livro. A partir disso, eu chamei o método calcularDesconto() da classe Produto na classe Livro por meio do super(), de modo que a referência para o desconto dos livros fosse o this.desconto = 0.2 (que está no construtor da classe Livro). Nela, eu também acrescentei o atributo autor. Tudo isso está materializado no código a seguir.
</p> <br>

<h3>CÓDIGO</h3>

```javascript
//Classe Produto.
class Produto {
    //Método construtor da classe Produto.
    constructor(nome, preco) {
        this.nome = nome;
        this.preco = preco;
        this.desconto = 0.1; //Esse aqui é o desconto fixo de 10%.
    }

    calcularDesconto() {
        //Variáveis do valor a ser descontado e do preço final do produto com o desconto de 10% do seu valor.
        var valorASerDescontadoDoPreco = this.preco * this.desconto;
        var precoFinalComDesconto = this.preco - valorASerDescontadoDoPreco;

        //Com este código, só será exibido "|Produto:" quando a classe do objeto criado posteriormente for Produto.
        if (this.constructor.name === "Produto") {
            console.log(`|Produto: ${this.nome}`);
        }

        //Mostrando o preço original, a porcentagem de desconto e valor do produto com desconto.
        console.log(`|Preço original: R$ ${this.preco.toFixed(2)}\n|Porcentagem de desconto: ${this.desconto * 100}%\n|Valor do produto com desconto: R$ ${precoFinalComDesconto.toFixed(2)}\n`);
    }
}

//Criação do objeto produto com a chamada do método calcularDesconto().
var produto = new Produto("Tênis", 100);
produto.calcularDesconto();


//Classe Livro (a palavra extends serve para indicar que a classe Livro está herdando da classe Produto).
class Livro extends Produto {
     //Método construtor da classe Livro.
    constructor(nome, preco, autor) {
        super(nome, preco); //Herdando nome e preço da classe Produto.
        this.autor = autor;
        this.desconto = 0.2; //Esse aqui é o desconto de 20%, que só é dado aos livros.
    }

    //Sobrescrevendo o método calcularDesconto da classe Produto.
    calcularDesconto() {
        console.log(`|Livro: ${this.nome}\n|Autor(a): ${this.autor}`);
        super.calcularDesconto();
    }
}

//Criando uma instância da classe Livro e chamando seu método calcularDesconto().
var livro = new Livro("Dom Casmurro", 30, "Machado de Assis");
livro.calcularDesconto();
```

