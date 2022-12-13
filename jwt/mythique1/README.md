# Mythique 1

Dans ce challenge, on se retrouve sur la page d'accueil du célèbre site de rencontre Mythique !

![jwt image](jwt1.PNG "mythique")

L'objectif est de se faire passer pour un administrateur pour récupérer le code d'invitation.

![jwt image](jwt2.PNG "mythique")

On récupère le Jwt stocké dans les cookies.

Sur le site JWT.io on remarque que le token est signé avec l'algorithme RS256

Une astuce bien connu sur la compromission de jwt token signé avec RS256 est de changer l'alg dans le header par HS256.

L'algorithme RS256 utilise une clé privée pour signer les messages, et une clé publique pour les vérifier. Si nous changeons l'algorithme de RS256 à HS256, la signature est maintenant vérifiée par l'algorithme HS256 en utilisant la clé publique comme clé secrète.

Une fois le header changé et le token signé avec notre propre clé on récupère le token suivant : eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE2NzA5NTA1OTAsImRhdGEiOnsibmFtZSI6Ik51YWdlIEljaSIsImlzQWRtaW4iOnRydWV9LCJpYXQiOjE2NzA5NDY5OTB9.xxjl6_26BrZPzoZfJA_Zoj3zrDKQP42dOwYn2mM-wqs

On remplace le jwt token de base par ce dernier. Puis on clique sur **Get Invite Code** et Bingo !
![jwt image](jwt3.PNG "mythique")
