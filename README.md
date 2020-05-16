# Cryptage/décryptage de fichiers

### Scripts minimalistes et commentés de cryptage/décryptage de fichiers sous Linux (scripts de type "Bash").

* Configuration de Bash en mode "strict" (debogage facilité).

* Ces outils comportent des "lanceurs" qui ouvrent une fenêtre console temporaire permettant d'exécuter le "cryptage/décryptage" proprement dit, de saisir le mot de passe et de s'assurer du bon déroulement.

* Lancement en mode graphique par double-clic sur les programmes "lanceurs" dans le navigateur de fichiers.

* Configurer les noms des fichiers "en clair" et "crypté" dans le corps des 2 scripts ".cryptage" et ".decryptage" avant le 1er lancement.

* Les fichiers à crypter peuvent être des archives contenant un nombre quelconque de fichiers.

* Pour ne pas encombrer le répertoire, les 2 scripts ".cryptage" et ".decryptage" sont en "fichiers cachés" (après suppression du "\_" à réaliser après téléchargement, ils commenceront par un ".").

* Je place le fichier crypté ansi que les 4 fichiers de l'outil dans un même répertoire pour constituer un ensemble autonome.

* L'algorithme de chiffrement choisi est "aes-256-cbc", c'est l'algorithme actuel le plus performant en terme de sécurité et rapidité.

* "OpenSSL" doit être installé sur le système.

* L'ensemble des fichiers de l'outil doivent être rendus exécutables.

* Avec la version que j'ai utilisée (OpenSSL 1.1.0i-fips  14 Aug 2018), le "salage" est automatique : pas besoin de le spécifier (option : "-salt" non reconnue) ; il change à chaque invocation de la commande "openssl aes-256-cbc" et il est mémorisé en début de fichier.

* Réalisé et exécuté sous Linux OpenSuse Leap ; bureau KDE ; sur PC 64 bits.

### Exemple d'utilisation

On dispose d'un fichier contenant des données sensibles que l'on veut protéger. On place ce fichier ainsi que les 4 fichiers de l'outil dans un même répertoire.

* Pour ouvrir ce fichier, afin de le consulter ou de le modifier, on doubleclic sur "decryptage_lanceur".

* On peut alors consulter et/ou modifier la copie en clair, générée par l'outil, à l'aide de l'éditeur approprié.

* Si on souhaite crypter et conserver la version que l'on vient de modifier, on doubleclic sur "cryptage_lanceur" => ATTENTION !!! la précédente version cryptée est remplacée par la version que l'on vient de modifier.

* On efface manuellement la copie en clair.

---
_Ces scripts, volontairement "sur-commentés", s'adressent aux débutants en scripting Bash._
_© Henri 13/05/20_
