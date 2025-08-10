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

# les branches sur git
les branches permettent de travailler sur des fonctionnalites ou des corrections
sans affecter la branche principale (master ou main)
pour afficher les branches existantes, on utilise la commande "git branch"
pour afficher la branche courante, on utilise "git branch --show-current"
pour renommer la branche courante, on utilise "git branch -m nouveau_nom"
pour creer une branche, on utilise la commande "git branch nom_de_branche"
pour basculer sur une branche, on utilise "git checkout nom_de_branche"
pour fusionner une branche dans la branche principale, on utilise "git merge nom_de_branche"
pour supprimer une branche, on utilise "git branch -d nom_de_branche"