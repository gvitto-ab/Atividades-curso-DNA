## Exercício 1 - Contando o faturamento
``` javascript
function somaFaturamento(valores) {
  var total = 0;
  for (var valor of valores) {
    total += valor;
  }
  return total;
}
somaFaturamento([1, 2, 3, 4]);
```

## Exercício 2 - Por quê não funciona?
O código não funciona porque o for...of só percorre objetos iteráveis, que possuem Symbol.iterator, como arrays e strings. Objetos literais comuns não são iteráveis, então o JavaScript não sabe como percorrê-los com esse laço. Para objetos, o correto é usar for...in, que itera sobre as propriedades.

## Exercício 3 - Agora vai funcionar
``` javascript

```

## Exercício 4 - Pare aqui senhor motorista
``` javascript

```

## Exercício 5 - Não vá por ali!
``` javascript

```
