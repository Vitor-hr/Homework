# Homework 1 - Aula 07_11

## Desafio

- Crie um array dinamico com tres posições [ 2, 1 ,2 ]
- crie uma interação que retorne numeros aleatórios entre 1 e 3
a cada retorno, altere o valor do array respectivamente

- utilizar as linhas ja codificadas e inserir em uma função
- crie uma verificação que identifica se os numeros do array são iguais; se sim:  escreva 'Porta 1: aberta', se nao: escreva 'Tente novamente'

- crie uma variavel de controle para acumular a quantidade de vezes que os numeros se repetem
- crie uma variavel que armazene o valor do ultimo sorteio
*compare o valor do ultimo sorteio com o valor do sorteio atual 
-- se os valores forem iguais, escreva : 'Porta (x) : aberta'
-- se os valores forem diferentes, escreva : 'Tente de novo' ( com a exceção do resultado ser de numeros iguais)

As portas serão abertas quando:
- os numeros do array forem iguais
- a sequencia de numero do array foi igual a sequencia de numeros do ultimo sorteio

Fim do jogo acontece quando a terceira porta for aberta.

---

## Logica

```Javascript
function saoTodosIguas(array) {
            return array[0] === array[1] && array[1] === array[2]
        }//função de verificação se os indices do array são iguais

        function jogo() {
            let array = [2, 1, 2]
            for (let i = 0; i < array.length; i++) {
                array[i] = Math.floor(Math.random([i]) * 3) + 1
            }//laço para sortear o array aleatorio

            if (saoTodosIguas(array)) {
                if (array[0] === 3) {
                    console.log("Fim de jogo")
                } else {
                    console.log(`porta ${array[0]} aberta!`)
                }
            } else {
                console.log("Tente novamente")
            }
        }
        jogo()

```