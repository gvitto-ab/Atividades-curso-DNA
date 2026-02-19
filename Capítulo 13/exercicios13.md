## Exercício 1 - Gastando até o que não tem
``` javascript
function calculaPrecoTotal(...precos) {
  return precos.reduce((total, preco) => total + preco, 0)
}

calculaPrecoTotal(1, 2, 3, 4, 5)
```

## Exercício 2 - Eu sou maior do que você, lero lero!
``` javascript
function todosSaoMaioresQue(referencia, ...numeros) {
  return numeros.every(numero => numero > referencia)
}

todosSaoMaioresQue(2, 3, 4, 5, 6, 7)
todosSaoMaioresQue(5, 4, 3, 2, 1)
todosSaoMaioresQue(1, 2)
```

## Exercício 3 - Bingo!
``` javascript
function anunciaBolasSorteadas(...bolas) {
  for (let i = 0; i < bolas.length; i++) {
    console.log(`A bola escolhida foi: ${bolas[i]}`)
  }
}

anunciaBolasSorteadas(1, 2, 3)
```

## Exercício 4 - Mas o professor que ensinou assim!
 O operador sempre interpreta as últimas variáveis passadas na função para compactá-las em um único Array. Apesar de a separação parecer fazer sentido para o aluno, não funcionará como esperado. O correto seria fazer algo do gênero:

``` javascript
function numerosELetras(...numerosELetras) {
  // corpo
```

## Exercício 5 - Este sim saber argumentar
Esse objeto existe automaticamente dentro de todas as funções em JavaScript e guarda todos os argumentos passados na chamada da função. Cada argumento fica armazenado em uma posição numérica, começando pelo índice 0.
