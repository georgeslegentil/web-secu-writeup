
## SSRF 

Dans ce challenge on arrive sur une page qui nous demande de récupérer un flag en nous rendant sur 

```URL
https://ssrf1.secu-web.blackfoot.dev/secret
```

```JSON
{
ok: false,
message: "You have to come from 127.0.0.1 not 172.21.0.8 :)",
flag: ""
}
```

Bien sûr on obtient cette réponse. On va donc essayer de trouver un moyen de détourner cette vérification côté serveur.

