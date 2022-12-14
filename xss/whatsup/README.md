
# Whatsup

Challenge d'injection XSS. 

On se retrouve sur l'interface d'un site de messagerie. On se doute rapidement que l'objectif ici est de récupérer le cookie stocké par le biais d'une injection dans l'input d'envoie de message.

On test alors l'envoi d'une balise ```HTML <script></script>```.
On remarque que cette balise est filtré
On remarque rapidement que les autres balises utilisées dans des injections ne sont pas filtrées et permettent ici l'injection.
Exemple avec cette injection : ```HTML <img/onerror="alert(1)"src=a> ```
