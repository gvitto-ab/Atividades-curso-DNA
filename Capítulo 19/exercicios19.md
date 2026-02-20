## Exercício 1 - Promessa verdadeira
Promises são objetos que representam o resultado de uma operação assíncrona, algo que pode dar certo, dar errado ou ainda estar em andamento; permitindo lidar com esse resultado no futuro de forma organizada.

## Exercício 2 - E que tudo mais vá para o inferno
Callback hell é o excesso de callbacks aninhados que deixa o código confuso. Promises resolvem isso ao organizar operações assíncronas de forma mais limpa e encadeada.

## Exercício 3 - Você cumpre as suas promessas?
``` javascript
function simulaPromise(sucesso) {
  return new Promise((resolve, reject) => {
    if (sucesso) {
      resolve('ok')
    } else {
      reject('not ok')
    }
  })
  .then(mensagem => console.log(mensagem))
  .catch(erro => console.log(erro))
}

simulaPromise(false)
simulaPromise(true)
```

## Exercício 4 - Você cumpre as suas promessas em tempo?
``` javascript
function simulaPromise(sucesso, delay) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      sucesso ? resolve('ok') : reject('not ok')
    }, delay)
  })
  .then(mensagem => console.log(mensagem))
  .catch(erro => console.log(erro))
}

simulaPromise(true, 2000)
simulaPromise(false, 1000)
```

## Exercício 5 - Passando promessa de pai para filho
O problema é que o segundo then não recebe o resultado do primeiro. Isso acontece porque o primeiro then não retorna nada, então o valor não é repassado para o próximo. Basta retornar o data no primeiro then e assim o valor flui corretamente de “pai para filho” na cadeia de Promises.

``` javascript
promise
  .then(data => {
    console.log(`resultado positivo: ${data}`)
    return data
  })
  .then(data => console.log(`resultado positivo 2: ${data}`))
  .catch(data => console.log(`resultado negativo: ${data}`))
```
