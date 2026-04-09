# Quest 3: Operadores Logicos

## O cenário

Na saída da Encruzilhada das Decisões, você encontra o **Salão dos Selos Duplos**. Ali, algumas portas não se abrem com apenas uma condição.

Às vezes, o herói precisa:

- ter a chave **e** coragem suficiente;
- ter ouro **ou** um passe especial;
- entrar apenas se **não** estiver amaldiçoado.

É aqui que entram os **operadores lógicos**.

Eles ajudam o programa a combinar condições, como se o herói precisasse analisar mais de uma regra antes de agir.

## O que você vai aprender

Nesta fase, sua missão é entender como:

- usar `and` para exigir mais de uma condição;
- usar `or` para aceitar caminhos diferentes;
- usar `not` para inverter uma condição;
- combinar operadores lógicos com `if`, `elif` e `else`;
- usar `input()` para deixar o jogador participar das decisões.

## A ideia principal

Até agora, você viu condições simples, como:

```python
vida = 80

if vida > 50:
    print("O heroi ainda consegue lutar.")
```

Mas em uma aventura real, muitas decisões dependem de mais de uma informação ao mesmo tempo.

## Usando `and`

O operador `and` significa:

"isso **e** aquilo precisam ser verdadeiros."

Exemplo:

```python
vida = 70
tem_escudo = "sim"

if vida > 50 and tem_escudo == "sim":
    print("O heroi pode entrar na arena.")
```

Nesse caso, não basta ter vida alta. Também é preciso estar com o escudo.

## Usando `or`

O operador `or` significa:

"basta que uma das condições seja verdadeira."

Exemplo:

```python
ouro = 10
tem_convite = "sim"

if ouro >= 50 or tem_convite == "sim":
    print("Voce pode entrar no baile real.")
```

Aqui, o herói pode entrar se tiver ouro suficiente **ou** se tiver um convite especial.

## Usando `not`

O operador `not` serve para inverter uma condição.

Exemplo:

```python
amaldiçoado = "nao"

if not amaldiçoado == "sim":
    print("Voce pode tocar no artefato sagrado.")
```

Isso quer dizer:

"se não estiver amaldiçoado, a ação é permitida."

Você também pode pensar assim:

```python
porta_trancada = False

if not porta_trancada:
    print("A porta esta aberta.")
```

## Tradução para o mundo RPG

Operadores lógicos ajudam em situações como:

- abrir uma porta se tiver chave **e** nível suficiente;
- permitir descanso se houver fogueira **ou** tenda;
- bloquear um altar se o herói estiver amaldiçoado;
- liberar uma missão apenas se o jogador tiver item raro **e** reputação alta;
- decidir fuga se a vida estiver baixa **ou** o inimigo for muito forte.

## Exemplo com escolha do jogador

```python
vida = int(input("Digite a vida do heroi: "))
tem_chave = input("Voce tem a chave dourada? ")

if vida >= 40 and tem_chave == "sim":
    print("Voce abre a porta do cofre.")
else:
    print("A porta continua fechada.")
```

Agora a decisão depende de duas condições ao mesmo tempo.

## Combinando escolhas

Você também pode montar decisões maiores:

```python
classe = input("Escolha sua classe: guerreiro, mago ou arqueiro: ")
mana = int(input("Digite a mana atual: "))

if classe == "mago" and mana >= 20:
    print("Voce consegue lançar a magia ancestral.")
elif classe == "arqueiro" or classe == "guerreiro":
    print("Voce tenta resolver o desafio de outro jeito.")
else:
    print("Ainda nao foi possivel agir.")
```

## Sua missão

Crie um programa que use operadores lógicos em situações de aventura.

Seu programa deve ter pelo menos:

- uma condição com `and`;
- uma condição com `or`;
- uma condição com `not`;
- pelo menos uma informação recebida com `input()`.

Você pode usar variáveis como:

- vida;
- ouro;
- nível;
- mana;
- chave mágica;
- item raro;
- estado de maldição;
- escolha do jogador.

## Ideias de missões

Você pode criar situações como:

- o herói só entra na torre se tiver chave **e** vida suficiente;
- o mercador vende o item se o herói tiver ouro **ou** um cupom da guilda;
- o altar libera a bênção se o herói **não** estiver amaldiçoado;
- o jogador pode fugir se tiver pouca vida **ou** se escolher recuar.

## Exemplo de inspiração

```python
vida = int(input("Vida do heroi: "))
ouro = int(input("Ouro do heroi: "))
tem_selo = input("Voce possui o selo da guilda? ")
amaldiçoado = input("O heroi esta amaldicoado? ")

if vida >= 50 and tem_selo == "sim":
    print("A passagem da montanha foi liberada.")

if ouro >= 100 or tem_selo == "sim":
    print("O mercador aceita negociar.")

if not amaldiçoado == "sim":
    print("Voce pode receber a bencao do templo.")
else:
    print("A energia sombria impede o ritual.")
```

## Desafio extra

Monte uma cena com 3 decisões seguidas:

1. verificar se o herói pode entrar em uma dungeon;
2. verificar se pode comprar uma poção rara;
3. verificar se pode usar um artefato mágico.

Tente usar operadores lógicos diferentes em cada etapa.

## Vitória da fase

Se você conseguir perceber que algumas decisões do programa dependem de mais de uma regra ao mesmo tempo e souber combinar essas regras com `and`, `or` e `not`, então desbloqueou uma habilidade importante do reino.
