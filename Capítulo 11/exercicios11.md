## Exercício 1 - Dando um trato no busão
``` javascript
const modelo = 'Mercedes-Benz Monobloco O-371 RSL';
const ano = 1993;
const capacidade = 50;

const busao = {
  modelo,
  ano,
  capacidade,
  acelerar() {
    console.log('vrum vrum');
  }
};
busao.acelerar();
```

## Exercício 2 - Corta isso fora
``` javascript
const dimensoes = (comprimento, alturaInicial) => {
  const altura = alturaInicial * 9 / 16;
  return { comprimento, altura };
};

console.log(dimensoes(10, 10));
// { comprimento: 10, altura: 5.625 }
```

## Exercício 3 - Oi, eu sou o Goku!
``` javascript
const pessoa = {
  nome: 'Goku',
  equipe: 'Guerreiro Z',
  seApresentar() {
    console.log(`Oi, eu sou o ${this.nome}!`);
  }
};

pessoa.seApresentar(); 
// Oi, eu sou o Goku!
```

## Exercício 4 - Criando à minha maneira
``` javascript
function criaObjetoComCaracteristicas(caracteristicas) {
  const objeto = {};

  for (const [chave, valor] of caracteristicas) {
    objeto[chave] = valor;
  }

  return objeto;
}

const caracteristicas = new Map();
caracteristicas.set('idade', 20);
caracteristicas.set('nome', 'Guilherme');

criaObjetoComCaracteristicas(caracteristicas);
```

## Exercício 5 - Esse tal de JSON
JSON é um formato leve para organizar e trocar dados, usando pares de chave e valor. Ele é muito usado para comunicação entre sistemas, como quando uma aplicação consome dados de uma API, por ser simples, legível e fácil de processar.