## Exercício 1 - Sei tudo sobre variáveis
a) Será exibido o número 10, diversas vezes.
b) Alterando o uso do `var` para utilizar o `let`.

## Exercício 2 - ISSO_EH_UMA_CONSTANTE
Com o ES6, a melhor forma de representar uma constante é usando a palavra‑chave const. Ela deixa claro que o valor não deve ser reatribuído, além de o próprio JavaScript impedir mudanças acidentais. Assim, em vez de só confiar no nome em caixa alta, o código fica mais seguro, legível e expressa melhor a intenção de que aquele valor é fixo.

## Exercício 3 - Eu estou mandando atribuir!
Com o ES6, a melhor forma de representar uma constante é usando a palavra‑chave **`const`**. Ela deixa claro que o valor não deve ser reatribuído, além de o próprio JavaScript impedir mudanças acidentais. Assim, em vez de só confiar no nome em caixa alta, o código fica mais seguro, legível e expressa melhor a intenção de que aquele valor é fixo.


## Exercício 4 - Pode ou não pode?
Esse código funciona porque `const` não torna o valor imutável, ele apenas impede que a referência seja trocada. No exemplo, a variável `jogador` continua apontando para o mesmo objeto, então é permitido alterar ou adicionar propriedades dentro dele. O que não seria possível é fazer algo como `jogador = {}` novamente. Em resumo, `const` protege a referência, não o conteúdo do objeto.


## Exercício 5 - Lá vem um temporal
A Temporal Dead Zone (TDZ) é o período em que uma variável declarada com let ou const existe no escopo, mas ainda não pode ser acessada, pois sua execução não chegou à declaração. Ela está ligada ao hoisting porque essas variáveis até são “erguidas” para o topo do escopo, mas não são inicializadas, e qualquer acesso antes da declaração gera erro. Em resumo: há hoisting, mas com acesso bloqueado até a declaração.

## Exercício 6 - Tudo fora de escopo
``` javascript
const status = [
  { codigo: 'OK', resposta: 'Sucesso' },
  { codigo: 'FAILED', resposta: 'Erro' },
  { codigo: 'PENDING', resposta: 'Pendente' }
];

let mensagem = '';
const codigoAtual = 'OK';

for (let i = 0; i < status.length; i++) {
  if (status[i].codigo === codigoAtual) {
    mensagem = status[i].resposta;
  }
}

console.log(mensagem);
```