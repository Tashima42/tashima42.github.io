---
layout: post
title:  "JavaScript fácil: Coerção de tipos"
date:   2020-04-14 12:31:08 -0300
categories: programacao javascript
---

![https://medium.com/javascript-in-plain-english/javascript-for-absolute-beginners-519dca78ce4a](https://cdn-images-1.medium.com/max/800/0*2fWXeXHk6wLueuhZ.jpg)

## Tipos de dados em Javascript

Em JavaScript a tipagem de dados é dinâmica, isso quer dizer que ao reservar um espaço na memória, não é necessário declarar para que tipo de dado aquele espaço será usado.
Ex: var minhaIdade = 18; Nesse caso, a variável contém um dado de tipo numérico, porém, diferente de Java ou C, é possível simplesmente atribuir outro tipo de dado sem nenhum problema. minhaIdade = "Não te interessa"; agora a variável minhaIdade contém um texto. Para uma explicação mais detalhada, recomendo a leitura deste texto.

***

## A coerção

Responda a seguinte pergunta: Quanto é 345 + vermelho?
Ela não faz sentido, não? Lógico que não. vermelho não é um número. Para seu computador isso também não faz. 
Quando uma operação não faz sentido, os valores são convertidos automaticamente para que passe a fazer. Isso é a coerção de tipos.
Ex:
- Código: 
``` js
var numeroExemplo = 345; //atribuindo um número
var palavraExemplo = 'vermelho'; //atribuindo um texto
var resultado = numeroExemplo + palavraExemplo; //somando o numero e o texto
console.log(resultado); //Mostrando no console o resultado
```
- Console: 
```
>"345vermelho"
```

Nesse exemplo, o número 345 foi convertido para o "texto" 345. Por mais estranho que isso possa parecer, é possível entender melhor com os próximos exemplos.

- Código: 
``` js
var numeroUm = 1; //declarando 1 como valor numérico
var palavraUm = '1'; //declarando 1 como um texto
var resultado = numeroUm + palavraUm; //somando as duas variáveis
console.log(resultado); //Mostrando no console o resultado
```
- Console: 
```
>"11"
```

Obviamente 1+1 é igual a 2, mas o console nos mostra 11. O que aconteceu? A variável palavraUm continha um texto e da mesma maneira que no exemplo anterior, então o computador transformou numeroUm também em um texto e concatenou os dois.

>**_con·ca·te·nar_**  
>(latim concateno, -are)  
>verbo transitivo e pronominal  
>_Estabelecer(-se) relação ou .sequência lógica entre ideias ou argumentos. = **ENCADEAR, JUNTAR, LIGAR**_

Ou seja, ele juntou os textos, da mesma maneira que acontece se fizermos o seguinte:

- Código: 
``` js
var meuNome= 'Pedro'; //declarando um texto
var meuSobrenome= 'Tashima'; //declarando um texto
var resultado = numeroUm + palavraUm; //concatenando os textos
console.log(resultado); //Mostrando no console o resultado
```
- Console: 
```
>"PedroTashima"
```

***

Agora sim tudo voltou a fazer sentido, 1 + 1 ainda é 2 e você entende o conceito de coerção de tipos, mas para não passar vergonha falando que 1 + 0 é 10, você deveria ver os seguintes links para entender mais do assunto (e ver minhas referências também):
- [Explicação mais detalhada do que é coerção de tipos](https://medium.com/trainingcenter/explicando-a-coer%C3%A7%C3%A3o-de-tipos-em-javascript-d6c9203c4e5)
- [Documentação da Mozilla e a diferença entre coerção e conversão](https://medium.com/r/?url=https%3A%2F%2Fdeveloper.mozilla.org%2Fen-US%2Fdocs%2FGlossary%2FType_coercion)
- [Representação visual do que acontece na prática](https://medium.com/r/?url=https%3A%2F%2Fdorey.github.io%2FJavaScript-Equality-Table%2F)
- [Livro: Javascript: Básico ao Avançado: Guia completo para iniciantes](https://medium.com/r/?url=https%3A%2F%2Fwww.amazon.com%2FJavascript-B%25C3%25A1sico-ao-Avan%25C3%25A7ado-Portuguese-ebook%2Fdp%2FB07F36KXNW)
- [Outra explicação, caso você não entenda as outras](https://medium.com/r/?url=https%3A%2F%2Fcrisgon.github.io%2Fposts%2FCoercao-de-tipos-javascript%2F)
