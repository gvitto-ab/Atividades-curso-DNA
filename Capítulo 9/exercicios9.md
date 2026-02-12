## Exercício 1 - Lista de compras
``` javascript
function tag(strings, ...valores) {
  const itens = valores[0]
    .split(',')
    .map(item => `<li>${item}</li>`)
    .join('');

  return `<ul>${itens}</ul>`;
}

const compras = 'leite,feijão,arroz,mandioca';
const elemento = tag`${compras}`;

console.log(elemento);
```

## Exercício 2 - Maçaroca de Strings
``` javascript

```

## Exercício 3 - Quero o seu endereço completo
``` javascript

```

## Exercício 4 - Seja muito bem-vindo!
``` javascript

```

## Exercício 5 - Cálculo interpolado
``` javascript

```
