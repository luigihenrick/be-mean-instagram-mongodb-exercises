##Exercício 2

##CRIAR DB POKEMONS
```
> use be-mean-pokemons
switched to db be-mean-pokemons

> show dbs
admin             → 0.000GB
be-mean           → 0.005GB
be-mean-instagram → 0.000GB
be-mean-teste     → 0.000GB
local             → 0.000GB
```

##INSERIR NO MINIMO 5 POKEMONS
```
> var pokemon = {"name":"Blastoise","description":"atira balas de agua","type":"água","attack":48,"defense":"cria um escudo de agua","height":0.5}
> db.pokemons.insert(pokemon)
Inserted 1 record(s) in 145ms
WriteResult({
  "nInserted": 1
})
> var pokemon = {"name":"Butterfree","description":"atira flores","type":"voa","attack":59,"defense":"paralisa o oponente","height":0.7}
> db.pokemons.insert(pokemon)
Inserted 1 record(s) in 2ms
WriteResult({
  "nInserted": 1
})

> var pokemon = {"name":"Arbok","description":"picada venenosa","type":"rastejante","attack":79,"defense":"espiral de aço","height":0.8}
> db.pokemons.insert(pokemon)
Inserted 1 record(s) in 2ms
WriteResult({
  "nInserted": 1
})

> var pokemon = {"name":"Beedrill","description":"ataque em enxame","type":"voa","attack":95,"defense":"escudo de abelhas","height":0.11}
> db.pokemons.insert(pokemon)
Inserted 1 record(s) in 2ms
WriteResult({
  "nInserted": 1
})

> var pokemon = {"name":"Arcanine","description":"super veloz","type":"tipo atlético","attack":100,"defense":"fulga ultra rápida","height":0.11}
> db.pokemons.insert(pokemon)
Inserted 1 record(s) in 4ms
WriteResult({
  "nInserted": 1
})
```

##EXIBIR COLLECTIONS DO DB POKEMONS
```
> show collections
pokemons → 0.001MB / 0.035MB
```

##EXIBIR POKEMONS DA COLLECTIONS
```
> db.pokemons.find()
{
  "_id": ObjectId("58b45b07be365e7ac9eb7c00"),
  "name": "Blastoise",
  "description": "atira balas de agua",
  "type": "água",
  "attack": 48,
  "defense": "cria um escudo de agua",
  "height": 0.5
}
{
  "_id": ObjectId("58b45baebe365e7ac9eb7c01"),
  "name": "Butterfree",
  "description": "atira flores",
  "type": "voa",
  "attack": 59,
  "defense": "paralisa o oponente",
  "height": 0.7
}
{
  "_id": ObjectId("58b45c4fbe365e7ac9eb7c02"),
  "name": "Arbok",
  "description": "picada venenosa",
  "type": "rastejante",
  "attack": 79,
  "defense": "espiral de aço",
  "height": 0.8
}
{
  "_id": ObjectId("58b45cbebe365e7ac9eb7c03"),
  "name": "Beedrill",
  "description": "ataque em enxame",
  "type": "voa",
  "attack": 95,
  "defense": "escudo de abelhas",
  "height": 0.11
}
{
  "_id": ObjectId("58b45d56be365e7ac9eb7c04"),
  "name": "Arcanine",
  "description": "super veloz",
  "type": "tipo atlético",
  "attack": 100,
  "defense": "fulga ultra rápida",
  "height": 0.11
}
Fetched 5 record(s) in 37ms
```

##CRIAR QUERY BUSCANDO POKEMON PELO NOME E ARMAZENAR NA VARIÁVEL POKE
```
> var query = {name: "Beedrill"}
> var poke = db.pokemons.findOne(query)
> poke
{
  "_id": ObjectId("58b45cbebe365e7ac9eb7c03"),
  "name": "Beedrill",
  "description": "ataque em enxame",
  "type": "voa",
  "attack": 95,
  "defense": "escudo de abelhas",
  "height": 0.11
}
```

##ALTERAR O VALOR DO DESCRIPTION DO POKEMON DESEJADO
```
> poke.description = "ataca em conjunto com seu enxame mortal"
ataca em conjunto com seu enxame mortal
```

##EXIBIR ALTERAÇÃO REALIZADA.
```
> poke
{
  "_id": ObjectId("58b45cbebe365e7ac9eb7c03"),
  "name": "Beedrill",
  "description": "ataca em conjunto com seu enxame mortal",
  "type": "voa",
  "attack": 95,
  "defense": "escudo de abelhas",
  "height": 0.11
}
```