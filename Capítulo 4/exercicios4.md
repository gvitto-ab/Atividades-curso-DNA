## Exercício 1 - Você está muito longe
``` javascript
function calculaDistancia(ruas) {
  var total = 0;
  for (var rua of ruas) {
    total += rua.tamanho;
  }
  return total;
}
var ruas = [
  { nome: 'Rua 1', tamanho: 2500 },
  { nome: 'Rua 2', tamanho: 3400 },
  { nome: 'Rua 3', tamanho: 1400 }
];
calculaDistancia(ruas);
```

## Exercício 2 - Tem alguém ai?
``` javascript
function isListaVazia(lista) {
  var iterador = lista[Symbol.iterator
  return iterador.next().done;
}
isListaVazia([]);
isListaVazia([1, 2, 3]);
```

## Exercício 3 - S-o-l-e-t-r-a-n-d-o
``` javascript

```

## Exercício 4 - Eu prefiro o meu
``` javascript

```
