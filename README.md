# === Introduction ===

Ce fichiers README.md à pour but d'expliquer l'ensemble des choix et configurations effectuer sur ce projet git.

# === Workflow choisi ===

Ce projet est basé sur la developpement d'un jeu vidéo.

Le workflow à donc été défini de la sorte:

master ==> Version de production du projet

hotfixes ==> Correctifs impromptus du projet (merge directement vers master)

releases ==> Versions majeures du projet (merge directement vers master et merge vers dev pour correction de bugs)

dev ==> Versions de développement qui ajoute les différentes fonctionnalités et corrige les bugs (merge vers release)

features ==> Fonctionnalités à ajoutés, scindé en 2 dossiers: /WIP pour les fonctionnalités futures en cours de developpement et /to-do pour les fonctionnalités à concevoir (merge directement vers dev)

# === Fonctionnalités du projet ===

Tous les commits, peu importe d'où ils sont fait, sont signés et vérifiés.

# --- Procédure ---

Tout d'abord il faut générer une clé GPG en suivant ses différentes étapes:

gpg --full-generate-key

Remplir les informations demandées

gpg --list-secret-keys --keyid-format=long

./Users/test/.gnupg/secring.gpg

------------------------------------


sec   4096R/[3AA5C34371567BD2] 2016-03-10 [expires: 2017-03-10]

uid                            Test 

ssb   4096R/42B317FD4BA89E7A   2016-03-10

L'ID de la clé est le code contenu dans les []

$ gpg --armor --export 3AA5C34371567BD2

Affiche l'ID de la clé GPG, au format ASCII armor

-----BEGIN PGP PUBLIC KEY BLOCK-----

exampleexampleexampleexampleexampleexampleexampleexampleexampleexampleexampleexample
exampleexampleexampleexampleexampleexampleexampleexampleexampleexampleexampleexample
exampleexampleexampleexampleexampleexampleexampleexampleexampleexampleexampleexample

...

---END PGP PUBLIC KEY BLOCK-----

Il suffit ensuite d'ajouter cette clé sur github.com dans l'espace "Settings > "SSH and PGP keys" > "New PGP Keys"
