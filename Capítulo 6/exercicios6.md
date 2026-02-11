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
Usamos **`Map`** quando lidamos com **coleções de dados mais dinâmicas**, em que as chaves podem mudar, ser adicionadas ou removidas com frequência, e quando precisamos percorrer ou consultar esses dados com facilidade. Já o **objeto literal** é mais indicado quando queremos representar algo fixo, como um registro com propriedades bem definidas, que fazem parte do significado daquele objeto.


## Exercício 4 - Professor, quando eu vou usar isso na minha vida?
Um uso simples de WeakMap é guardar dados privados ligados a um objeto, que desaparecem automaticamente quando o objeto deixa de existir:
``` javascript
var dadosPrivados = new WeakMap();

var usuario = {};
dadosPrivados.set(usuario, { senha: '123' });

dadosPrivados.get(usuario);
```
Esse padrão é útil quando queremos associar informações a objetos sem expô-las e sem risco de vazamento de memória.

## Exercício 5 - Não vou mais com a sua cara.
``` javascript
function deletaAmigos(amigos, exAmigos) {
  for (var nome of exAmigos) {
    if (amigos.has(nome)) {
      amigos.delete(nome);
      console.log('foi deletado!');
    } else {
      console.log('não é seu amigo!');
    }
  }
}

var amigos = new Map();
amigos.set('João Silva', { idade: 23, sexo: 'masculino' });
amigos.set('Luisa Pimenta', { idade: 18, sexo: 'feminino' });
amigos.set('Julio Marinho', { idade: 52, sexo: 'masculino' });
amigos.set('Marcela Mel', { idade: 27, sexo: 'feminino' });

deletaAmigos(amigos, ['João Silva', 'Carlos']);
```