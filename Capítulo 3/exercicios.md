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
function buscar(propriedade, valor, lista) {
  return lista.find(function (item) {
    return item[propriedade] === valor;
  });
}

var lista = [
  { nome: 'Tânia', sobrenome: 'Cardoso', idade: 65 },
  { nome: 'Emilly', sobrenome: 'Barbosa', idade: 46 },
  { nome: 'Vitória', sobrenome: 'Costa', idade: 83 },
  { nome: 'Erick', sobrenome: 'Ferreira', idade: 16 }
];

buscar('nome', 'Tânia', lista);
```

## Exercício 8 - Calculadora Humana
``` javascript
function calculaAreaTotal(dimensoes) {
  return dimensoes.reduce(function (total, dimensao) {
    return total + (dimensao.altura * dimensao.comprimento);
  }, 0);
}

var dimensoes = [
  { altura: 10, comprimento: 20 },
  { altura: 2, comprimento: 4 },
  { altura: 1, comprimento: 1 },
  { altura: 50, comprimento: 50 }
];

calculaAreaTotal(dimensoes);
```

## Exercício 9 - Raízes Quadradas
``` javascript
function calculaRaizesQuadradas(numeros) {
  return numeros.map(function (numero) {
    return Math.sqrt(numero);
  });
}

calculaRaizesQuadradas([1, 4, 9, 16, 25]);
```

## Exercício 10 - E tem alguma diferença?
O **forEach** e o **map** percorrem um array elemento por elemento, mas têm propósitos diferentes: o **forEach** é usado quando você quer apenas executar uma ação para cada item, como imprimir valores ou alterar algo externo, e por isso **não retorna nada**; já o **map** é usado quando você quer **transformar os elementos do array**, pois ele cria e retorna **um novo array** com o resultado dessa transformação, sem modificar o array original.


## Exercício 11 - A pequena ovelha Dolly
``` javascript
function clonaObjeto(objeto) {
  var copia = {};

  Object.getOwnPropertyNames(objeto).forEach(function (propriedade) {
    copia[propriedade] = objeto[propriedade];
  });

  return copia;
}

clonaObjeto({ nome: 'Dolly', idade: 5 });
```

## Exercício 12 - Limpando o estoque
``` javascript
function existeProdutosDatados(produtos, dataReferencia) {
  var dataBase = dataReferencia ? new Date(dataReferencia) : new Date();

  return produtos.some(function (produto) {
    return new Date(produto.dataValidade.split('/').reverse().join('-')) < dataBase;
  });
}

var produtos = [
  { nome: 'Cereal', preco: 10, dataValidade: '21/02/2017' },
  { nome: 'Suco de Abacaxi', preco: 12, dataValidade: '01/01/2017' },
  { nome: 'Torta de frango', preco: 25, dataValidade: '07/07/2017' }
];

existeProdutosDatados(produtos, '2017-03-01');
```