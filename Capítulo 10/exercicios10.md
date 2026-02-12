## Exercício 1 - Hora de usar as setas
``` javascript
let carrinho = [
  { nome: 'abacaxi', preco: '2.00' },
  { nome: 'detergente', preco: '2.50' },
  { nome: 'bolacha', preco: '3.80' }
];

const imprimeProduto = (nome, preco) =>
  console.log(`Produto: ${nome} | Preço: ${preco}`);

carrinho.forEach(produto =>
  imprimeProduto(produto.nome, produto.preco)
);
```

## Exercício 2 - Hora de usar as setas novamente
``` javascript
let itens = ['abacaxi', 'banana', 'maçã', 'laranja', 'limão'];

itens.forEach(item => console.log(item));
```

## Exercício 3 - Quem está na janela?
Isso acontece porque, no navegador, o escopo global é o próprio objeto `window`. Então, quando uma função é declarada fora de qualquer objeto ou módulo, o JavaScript associa automaticamente o `this` ao `window`, já que ele representa o contexto global da aplicação.


## Exercício 4 - Vou lavar sua boca com sabão!
``` javascript
let palavroes = [
  'Inconstitucionalíssimo',
  'Otorrinolaringologista',
  'Pneumoultramicroscopicossilicovulcanoconiose',
  'Oftalmotorrinolaringologista'
];

let tamanhos = palavroes.map(palavra => palavra.length);

console.log(tamanhos);
```

## Exercício 5 - Tudo dentro do seu escopo
``` javascript
var equipe = {
  nome: 'Valentes da Glória',
  membros: ['Luciano', 'Maria', 'Virginia', 'Daniela'],
  imprimeNomes: function () {
    this.membros.forEach(membro =>
      console.log(`${membro} é da equipe ${this.nome}`)
    );
  }
};

equipe.imprimeNomes();
```
