# Quest 6: Dict

## O cenário

Depois de organizar itens em listas no Mercado das Mochilas Infinitas, você segue viagem até o **Arquivo dos Cronistas**. Nesse lugar, os aventureiros não guardam apenas coleções de objetos. Eles também registram fichas completas com informações diferentes sobre cada herói, criatura ou tesouro.

Esses registros mágicos funcionam como os **dicionários**.

Em Python, um dicionário serve para guardar informações usando uma lógica de:

- **chave** para identificar o dado;
- **valor** para guardar a informação.

É como montar uma ficha em que cada campo tem um nome claro.

## O que você vai aprender

Nesta fase, sua missão é entender como:

- criar um dicionário;
- guardar informações diferentes em uma mesma estrutura;
- acessar valores por chave;
- alterar valores já existentes;
- adicionar novos dados;
- usar dicionários para representar fichas de heróis, inimigos ou baús.

## A ideia principal

Uma lista guarda elementos por posição.

Um dicionário guarda elementos por **nome de campo**.

Exemplo:

```python
heroi = {
    "nome": "Luna",
    "classe": "maga",
    "vida": 100,
    "ouro": 50
}
```

Nesse caso:

- `"nome"` é uma chave;
- `"Luna"` é o valor guardado nessa chave;
- `"vida"` é outra chave;
- `100` é o valor associado a ela.

## Acessando informações

Para consultar um valor do dicionário, usamos a chave:

```python
print(heroi["nome"])
print(heroi["vida"])
```

Isso faz bastante sentido em um RPG, porque o código fica mais fácil de ler do que várias variáveis soltas.

## Alterando valores

Assim como acontece com variáveis, os dados também podem mudar durante a aventura.

```python
heroi = {
    "nome": "Luna",
    "vida": 100,
    "ouro": 50
}

heroi["vida"] = 80
heroi["ouro"] = 75

print(heroi)
```

Aqui o herói perdeu vida e ganhou mais ouro.

## Adicionando novos campos

Você também pode criar novas informações depois que o dicionário já existe.

```python
heroi = {
    "nome": "Luna",
    "classe": "maga"
}

heroi["arma"] = "cajado antigo"

print(heroi)
```

Agora a ficha do herói passou a ter também uma arma equipada.

## Usando `input()` com dicionários

Como este projeto é uma aventura guiada, faz sentido deixar o jogador preencher a própria ficha.

```python
nome = input("Nome do heroi: ")
classe = input("Classe do heroi: ")
vida = int(input("Vida inicial: "))
ouro = int(input("Ouro inicial: "))

heroi = {
    "nome": nome,
    "classe": classe,
    "vida": vida,
    "ouro": ouro
}
```

Desse jeito, o dicionário organiza os dados recebidos pelo teclado.

## Tradução para o mundo RPG

Dicionários são úteis para representar:

- a ficha completa do herói;
- os dados de um inimigo;
- o conteúdo de um baú;
- os status de uma sala;
- uma missão com nome, recompensa e dificuldade.

Em vez de espalhar as informações em muitas variáveis separadas, você reúne tudo em um só lugar com nomes claros.

## Exemplo com ficha de inimigo

```python
inimigo = {
    "nome": "Goblin Sombrio",
    "vida": 40,
    "ataque": 12,
    "ouro_derrotado": 15
}

print(inimigo["nome"])
print(inimigo["ataque"])
```

## Misturando com o que voce ja aprendeu

Você também pode usar condicionais com dicionários:

```python
heroi = {
    "nome": "Arin",
    "vida": 25,
    "pocoes": 2
}

if heroi["vida"] < 30:
    print("O heroi esta em perigo.")
```

Ou atualizar uma ficha depois de um evento:

```python
heroi["pocoes"] = heroi["pocoes"] - 1
heroi["vida"] = heroi["vida"] + 20
```

## Sua missão

Crie uma ficha de personagem usando um dicionário.

Seu programa deve:

- pedir ao jogador pelo menos 4 informações com `input()`;
- usar `int()` nos valores numéricos;
- guardar tudo em um dicionário;
- mostrar pelo menos 3 campos da ficha usando as chaves;
- alterar pelo menos um valor durante a aventura;
- adicionar pelo menos um novo campo à ficha.

## Sugestões de campos

Você pode usar informações como:

- nome;
- classe;
- vida;
- mana;
- ouro;
- arma;
- nível;
- poções;
- reino de origem.

## Exemplo de inspiração

```python
nome = input("Nome do heroi: ")
classe = input("Classe do heroi: ")
vida = int(input("Vida inicial: "))
ouro = int(input("Ouro inicial: "))

heroi = {
    "nome": nome,
    "classe": classe,
    "vida": vida,
    "ouro": ouro
}

print("Nome:", heroi["nome"])
print("Classe:", heroi["classe"])
print("Vida:", heroi["vida"])

heroi["ouro"] = heroi["ouro"] + 20
heroi["arma"] = "espada de bronze"

print(heroi)
```

## Desafio extra

Crie também um segundo dicionário para um inimigo ou um baú.

Exemplos:

- um goblin com nome, vida e ataque;
- um baú com tipo, ouro e item raro;
- uma sala com nome, perigo e recompensa.

Se quiser ir além, use uma condição para decidir o que acontece com a ficha do herói depois desse encontro.

## Vitória da fase

Se você conseguir olhar para várias informações diferentes sobre a mesma coisa e pensar:

"isso pode virar uma ficha com chaves e valores",

então desbloqueou uma ferramenta muito importante para organizar seu código em Pyland.
