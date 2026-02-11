## Exercício 1 - Par ou ímpar?
``` javascript
var numeros = [0, 1, 2, 3, 4, 5];

numeros.forEach(function (numero) {
  if (numero % 2 === 0) {
    console.log(numero + ' é par');
  } else {
    console.log(numero + ' é ímpar');
  }
});
```

## Exercício 2 - Quero o dobro
``` javascript
function dobrar(numeros) {
  return numeros.map(function (numero) {
    return numero * 2;
  });
}

dobrar([1, 2, 3]);
```

## Exercício 3 - NÃO ESTOU BRAVO
``` javascript
function caps(palavras) {
  return palavras.map(function (palavra) {
    return palavra.toUpperCase();
  });
}

caps(['oi', 'tudo', 'bem?']);
```

## Exercício 4 - Equilibrio de parênteses
``` javascript
function validaParenteses(parenteses) {
  var arrayParenteses = parenteses.split('');

  var soma = arrayParenteses.reduce(function (total, caractere) {
    if (total < 0) {
      return total;
    }

    if (caractere === '(') {
      return total + 1;
    }

    if (caractere === ')') {
      return total - 1;
    }

    return total;
  }, 0);

  return soma === 0;
}
```

## Exercício 5 - Sem duplicações
``` javascript
function removeDuplicatas(numeros) {
  return numeros.reduce(function (resultado, numero) {
    if (!resultado.find(function (item) { return item === numero; })) {
      resultado.push(numero);
    }
    return resultado;
  }, []);
}

removeDuplicatas([1, 2, 3, 3, 4, 5]);
``
```

## Exercício 6 - Reprovado!
``` javascript
function aprovados(alunos, mediaMinima) {
  return alunos.filter(function (aluno) {
    return aluno.media >= mediaMinima;
  });
}

var alunos = [
  { nome: 'Diogo', media: 5.5 },
  { nome: 'Julia', media: 9.5 },
  { nome: 'Roberto', media: 1.5 },
  { nome: 'Tiago', media: 6.0 }
];

aprovados(alunos, 6.5);
```

## Exercício 7 - Dados precisos
``` javascript

```

## Exercício 8 - Calculadora Humana
``` javascript

```

## Exercício 9 - Raízes Quadradas
``` javascript

```

## Exercício 10 - E tem alguma diferença?



## Exercício 11 - A pequena ovelha Dolly
``` javascript

```

## Exercício 12 - Limpando o estoque
``` javascript

```