# Webdev – Serveur d&#39;application - Erreur de l&#39;accès natif MySQL, ERR\_TIMEOUT\_REQUEST

**Cas pratique**

Sur un serveur Linux, utilisation de webservice Windev, avec accès à une base mysql.

**Erreurs rencontrées**

Erreur de l&#39;accès Natif Mysq ou Erreur de Timeout.

**Version impactés**

Toutes versions confondues

# Messages d&#39;erreurs

## Cas 1

Que s&#39;est-il passé ?

Erreur de l&#39;accès natif MySQL.

Numéro d&#39;erreur = 27

La couche client MySQL n&#39;est probablement pas correctement installée.

Aucune bibliothèque d&#39;accès à MySQL n&#39;a été trouvée, le module libmysqlclient.so (xx bits) ou une de ses dépendances n&#39;a pas été chargé.

Code erreur : 73001

## Cas 2

La requête n&#39;a pas répondu dans le délai fixé (\&lt;DELAIS\&gt; secondes). ERR\_TIMEOUT\_REQUEST (22)

# Résolution :

Il faut récupérer la dll libmysqlclient.so d&#39;une installation mysql-client et la copier dans le dossier /usr/lib/ (Debian 8).

Dll disponible ici : libmysqlclient.so

**Attention :**** Il ne faut pas installer** mysql-client/mysql-server, au risque de voir désormais le webservice déployé tourner en boucle sans logs d&#39;erreurs.
