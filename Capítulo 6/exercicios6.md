## Exercício 1 - Você tem esse produto?
``` javascript
function possuiProduto(produtos, produtoDesejado) {
  return produtos.has(produtoDesejado);
}

var produtos = new Map();
produtos.set('Arroz', 7.10);
produtos.set('Feijão', 2.30);
produtos.set('Macarrão', 4.70);
produtos.set('Refrigerante', 3.00);

possuiProduto(produtos, 'Feijão');
```

## Exercício 2 - Comprinhas online
``` javascript
function calculaValorTotalDaCompra(produtos, cidade, caixa, fretes) {
  var total = 0;

  for (var produto of produtos) {
    total += caixa.get(produto);
  }
  if (fretes.has(cidade)) {
    total += fretes.get(cidade);
  } else {
    total += fretes.get('Outros');
  }
  return total;
}

var caixa = new Map();
caixa.set('Arroz', 7.10);
caixa.set('Feijão', 2.30);
caixa.set('Macarrão', 4.70);
caixa.set('Refrigerante', 3.00);

var fretes = new Map();
fretes.set('São Paulo', 10.10);
fretes.set('Rio de Janeiro', 12.30);
fretes.set('Brasília', 14.70);
fretes.set('Outros', 13.00);

calculaValorTotalDaCompra(['Arroz'], 'São Paulo', caixa, fretes);
```

## Exercício 3 - Não sei qual algoritmo usar hoje


## Exercício 4 - Professor, quando eu vou usar isso na minha vida?


## Exercício 5 - Não vou mais com a sua cara.
``` javascript

```