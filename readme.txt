## initialiser un projet 
creer le repertoire de projet et activer le suivi de version de controle 
initialiser le versionning avec "git init"
s'il ya des fichiers ou dossier dans le repertoire du projet, il faut les ajouter 
dans le suivi de version avec "git add ."

## realiser des modifications et prise en compte des modifications
apres avoir modifie des fichiers, 
il faut les ajouter au suivi de version avec "git add ."
puis il faut realiser un commit avec "git commit -m 'message de commit'"
le message de commit doit etre explicite et decrit les modifications effectuees

la commande "git statsus" permet de voir le status de vos modifications en cours
et prise ou non prise en compte dans les commit 


## inserer des coorectifs urgent retour anterieur a un commit 
Absolument. C'est un scénario très courant et une démonstration de la puissance de Git. 
Vous pouvez "remonter dans le temps" pour démarrer un nouveau travail, puis intégrer ce travail dans le présent.
Voici la marche à suivre, étape par étape.

Le scénario visuel
Pour bien comprendre, imaginons votre historique sur la branche main :
C1---C2---C3---C4---C5---C6---C7 (main)

Votre objectif est :
Partir du commit C2.
Créer une nouvelle branche et y ajouter un nouveau commit, appelons-le H.
Fusionner ce travail (H) avec C7 pour créer un nouveau commit C8 sur main.

afficher l'historique des commits : "git log --oneline --graph main"
1. **Créer une nouvelle branche à partir de C2** :
   ```bash
   git checkout -b new-branch C2
   ```
   ** exemple : "git checkout -b coorectif-urgent 724f98c" où 724f98c est l'identifiant du commit C2.

2. **Ajouter un nouveau commit H** :
   Modifiez les fichiers nécessaires, puis ajoutez et validez vos modifications :
   ```bash
   git add .
   git commit -m "Ajout du commit H"
   ```
3. **Revenir à la branche principale** :
   ```bash
   git checkout main
   ```
4. **Fusionner la nouvelle branche avec la branche principale** :
   ```bash
   git merge coorectif-urgent
   ```
5. **Vérifier l'historique des commits** :
   ```bash
   git log --oneline --graph main
   ```
