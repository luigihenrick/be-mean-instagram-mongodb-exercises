# MongoDB - Aula 01 - Exercício
autor: Luigi Henrick Feitoza Silva

## Importando os restaurantes

```
mongoimport --db be-mean --collection restaurantes --drop --file restaurantes.json 
2018-01-23T11:58:04.962-0200    connected to: localhost
2018-01-23T11:58:04.962-0200    dropping: be-mean.restaurantes
2018-01-23T11:58:05.857-0200    imported 25359 documents
```

## Contando os restaurantes

```
luigi(mongod-3.6.1) be-mean> db.restaurantes.find({}).count()
25359

```