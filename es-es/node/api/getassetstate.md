# Método Getassetstate

Devuelve el estado de un activo.


## Descripción de los parámetros

activo: id. del activo. 


## Ejemplo de llamada


http://node:10332?jsonrpc=2.0&method=getassetstate&params=["c56f33fc6ecfcd0c225c4ab356fee59390af8560be0e930faebe74a6daff7c9b"]&id=1

Petición:
```json
{
	"jsonrpc": "2.0",
	"method": "getaccountstate",
	"params": ["c56f33fc6ecfcd0c225c4ab356fee59390af8560be0e930faebe74a6daff7c9b"],
	"id": 1
}
```


Respuesta:
```json
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": {
        "version": 0,
        "id": "c56f33fc6ecfcd0c225c4ab356fee59390af8560be0e930faebe74a6daff7c9b",
        "type": "SystemShare",
        "name": [
            {
                "lang": "zh-CN",
                "name": "小蚁股"
            },
            {
                "lang": "en",
                "name": "AntShare"
            }
        ],
        "amount": "100000000",
        "available": "100000000",
        "precision": 0,
        "owner": "00",
        "admin": "Abf2qMs1pzQb8kYk9RuxtUb9jtRKJVuBJt",
        "issuer": "Abf2qMs1pzQb8kYk9RuxtUb9jtRKJVuBJt",
        "expiration": 4000000,
        "frozen": false
    }
}
```
