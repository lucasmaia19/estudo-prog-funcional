## Stream
* É uma sequencia de elementos advinda de uma fonte de  dados que oferece suporte a "operações agregadas".

# Operação intermediaria
* Produz uma nova streams (encadeamento)
* Só executa quando uma operação terminal é invocada (lazy evaluation)

Ex :

```
• filter
• map
• flatmap
• peek
• distinct
• sorted
• skip
• limit 
```

# Operação terminal 
* Produz um objeto não-stream (coleção ou outro)
* Determina o fim do processamento da stream

```
• forEach
• forEachOrdered
• toArray
• reduce
• collect
• min
• max
• count
• anyMatch 
• allMatch 
• noneMatch
• findFirst
• findAny 
```

