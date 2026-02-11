## Exercício 1 - Retirando o excesso
``` javascript
function removeDuplicatas(numeros) {
  return Array.from(new Set(numeros));
}

removeDuplicatas([1, 1, 2, 2, 3, 3]);
```

## Exercício 2 - Um é forte e o outro é fraco, não é isso?
A principal diferença é que o Set mantém referências fortes aos seus valores e permite armazenar qualquer tipo de dado, sendo ideal para listas sem repetição que podemos percorrer livremente. Já o WeakSet aceita apenas objetos, mantém referências fracas e não é iterável, o que faz com que seus itens sejam removidos automaticamente da memória quando não são mais usados, ajudando a evitar vazamentos de memória.

## Exercício 3 - Mas na minha máquina funciona!
O erro acontece por dois motivos ligados ao WeakSet.
Primeiro, o WeakSet não é iterável, então ele não pode ser usado com for...of. Segundo, o construtor do WeakSet espera um único iterável, e não vários argumentos separados. No código, além de tentar iterar, ele também passa os objetos de forma incorreta.

## Exercício 4 - Isso é completamente inútil!
Um exemplo simples de uso de WeakMap é guardar dados privados associados a um objeto, sem expô-los e sem risco de vazamento de memória:
``` javascript
var dadosPrivados = new WeakMap();
var usuario = {};

dadosPrivados.set(usuario, { senha: '123' });
dadosPrivados.get(usuario);
``` 