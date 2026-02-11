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


## Exercício 4 - Isso é completamente inútil!
