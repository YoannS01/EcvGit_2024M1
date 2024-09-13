Bonjour à tous,

Voici l'exercice à réaliser.
Pour la notation je regarderais l'arbre git et je vérifierais qu'il correspond bien à ce qui est demandé.
Normalement, vous avez un projet git qui a été créé en PUBLIC ! Attention, s'il n'est pas public, je ne pourrais pas vous noter !

Voici donc l'exercice :

# 1 - Mise en place (10 pts)
## Initialisation
- Effectuez un clone de ce projet (celui que vous êtes en train de lire) dans un dossier vide où vous avez accès sur votre machine : "git clone https://github.com/GuillaumeMuret/EcvGit_2024M1.git"
- Rendez-vous dans le dossier fraichement cloné
- Renommez le remote actuel suite au clone : "git remote rename origin github-gmuret"
- Ajouter votre remote comme indiqué sur la page de votre nouveau projet GitHub "git remote add origin git@github.com:<VOTRE_NOM_UTILISATEUR_GITHUB>/EcvGit_2024M1.git" (si vous vous êtes trompés sur l'url, il vous faudra supprimer origin "git remote rm origin" et refaire la commande d'ajout)
- Pousser la branche "master" sur le remote origin : "git push -u origin HEAD"
- (vous venez de réaliser ce qu'on appelle un fork)
- Créer une nouvelle branche "feature/heure-actuelle"
- Créer un nouveau fichier nommé "heure.txt" avec l'heure qu'il est actuellement sur la première ligne au format "HH:MM" où HH correspond aux heures et MM aux minutes (exemple il est 16h34 j'écris dans mon fichier 16:34)
- Ajouter le fichier "heure.txt" à l'index Git de la branche "feature/heure-actuelle"
- Effectuer un commit avec le message "Add current time"
- Pousser la branche "feature/heure-actuelle"
- Revenez sur "master"
- Créer une nouvelle branche "feature/date-et-heure"
- Créer un nouveau fichier nommé "date.txt" avec la date et l'heure actuelle sur la première ligne au format "AAAA-MM-DD_HH:MM" où :
    - AAAA correspond à l'année en cours (2024 pour info)
    - MM le mois (si on est en septembre ce serait donc 09)
    - DD le jour (si on est le 5 on écrit 05)
    - HH:MM respecte la même règle précédente avec les heures et minutes
- Ajouter le fichier "date.txt" à l'index Git de la branche "feature/date-et-heure"
- Effectuer un commit avec le message "Add current date"
- Pousser la branche "feature/date-et-heure"
- Revenir sur "master"
- Créer une nouvelle branche "feature/heure-courante"
- Créer un nouveau fichier nommé "heure.txt" avec sur la première ligne votre nom de famille en majuscule suivi de l'heure qu'il est actuellement au format "HH:MM" comme expliqué précédemment
- Ajouter le fichier "heure.txt" à la branche "feature/heure-courante"
- Effectuer un commit avec le message "Add name and current time"
- Pousser la branche "feature/heure-courante"

# 2 - Actions sur les branches (10 pts)
- Placer vous sur la branche "feature/heure-actuelle"
- Effectuer une fusion de "feature/date-et-heure" sur "feature/heure-actuelle"
- Garder le message de commit par défaut de la fusion ("Merge branch ..."). RAPPEL : pour quitter l'éditeur de texte vi il vous suffit de taper "ESC", entrer ces trois caractères ":wq" puis appuyer sur "ENTRER". Pour quitter l'éditeur de texte nano il vous suffit de taper "CTRL + O" pour écrire (sauvegarder) et "CTRL + X" pour quitter
- Pousser le résultat par défaut de cette fusion
- Effectuer une fusion de "feature/heure-courante" sur "feature/heure-actuelle"
- Le résultat à l'intérieur du fichier en conflit doit être la nouvelle heure actuelle au format vu précédemment
- Une fois le conflit résolu, ajouter le fichier en conflit à l'index Git permettant de valider la fusion
- Effectuer un commit avec le message "merge with conflict feature/date-et-heure into feature/heure-actuelle" permettant terminer la fusion
- Modifier le fichier "heure.txt" avec le contenu "Hakuna Matata" sur la première ligne
- Ajouter cette modification à l'index Git puis effectuer un commit avec le message "Quelle phrase magnifique"
- Pousser ce commit
- Supprimer le fichier "heure.txt"
- Ajouter cette suppression à l'index Git puis effectuer un commit avec le message "Quel chant fantastique"
- Effectuer un revert de l'action précédente ("git revert SHA1_DU_COMMIT_QUE_JE_VEUX_REVERT" pour trouver le "SHA1_DU_COMMIT_QUE_JE_VEUX_REVERT" il suffit de réaliser la commande "git log", les sha1 sont écrits juste après le mot commit)
- Poussez !
