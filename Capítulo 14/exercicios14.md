## Exercício 1 - Hora do ditado
``` javascript
const letras = ['e', 'c', 'm', 'a', 's', 'c', 'r', 'i', 'p', 't']

console.log(...letras)

```

## Exercício 2 - Não são só umas reticências?
Apesar de os dois usarem os três pontinhos (...), a ideia de cada um é oposta:

Rest junta vários valores e transforma tudo em um array.
Spread faz o contrário: pega um array (ou iterável) e espalha seus valores, usando cada item separadamente.

## Exercício 3 - Contador de Vogais
``` javascript
function contaQuantidadeVogaisNaoAcentuadas(...palavras) {
  const vogais = ['a', 'e', 'i', 'o', 'u']

  return palavras.reduce((total, palavra) => {
    return total + [...palavra].filter(letra => vogais.includes(letra)).length
  }, 0)
}

contaQuantidadeVogaisNaoAcentuadas('javascript', 'ecmascript')
```

## Exercício 4 - Esse jeito é tão ultrapassado...
É possível através do método `apply`:

``` javascript
var argumentos = [1,2,3];
console.log.apply(console, argumentos);
```

## Exercício 5 - A união faz a força
``` javascript
const equipeMarketing = ['Joana', 'Marcela', 'Bruna']
const equipeComercial = ['Talita', 'Luisa', 'Vitória']

const timeCompleto = [...equipeMarketing, ...equipeComercial]

realizaBrainstorm(timeCompleto)
```