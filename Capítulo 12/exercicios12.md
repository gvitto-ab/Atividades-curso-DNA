## Exercício 1 - O dobro de nada
``` javascript
mostraNome(); // Meu nome é: undefined
```
Na execução desse código, a função é chamada sem passar nenhum valor para o parâmetro nome. Como não há parâmetro padrão definido, o valor de nome será undefined.


## Exercício 2 - Me passa uns parâmetros ae
``` javascript
function soma(a = 0, b = 0) {
  return a + b;
}
```

## Exercício 3 - Tá aqui a minha identidade
``` javascript
function imprimeNomeCompleto(nome = '', sobrenome = '', nomeDoMeio = '') {
  console.log(`${nome} ${nomeDoMeio} ${sobrenome}`.trim());
}

imprimeNomeCompleto('João');
// João
```

## Exercício 4 - Adivinha em quem eu estou pensando?
O valor exibido será: `text valor 1`  Isso acontece porque o valor padrão do parâmetro x é avaliado antes da função ser executada, usando o v que está no escopo externo. A variável v declarada dentro da função só existe depois que o parâmetro já recebeu seu valor, então ela não interfere no valor de x.


## Exercício 5 - Pare de me imitar!
``` javascript
function subtrair(a = 0,b = a) {
  return a + b;
}
```
