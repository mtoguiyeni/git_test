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

# depot distant en ligne : github, gitlab, bitbucket
configurer un depot distant permet de partager le code avec d'autres personnes
por afficher les depots distants, on utilise la commande "git remote -v"

pour ajouter un depot distant, il faut d'abord le creer dans le github 
sur github : aller creer un nouveau repositoire : exemple : "git_test"

puis, dans le terminal, dans le repertoire du projet,
pour ajouter un depot distant, on utilise la commande "git remote add nom_du_depot url_du_depot"
exemple : "git remote add mtoguiyeni https://github.com/mtoguiyeni/git_test.git

pour creer un depot distant, on utilise la commande "git remote add origin url_du_depot"
exemple : "git remote add origin https://github.com/mtoguiyeni/git_test.git

pour envoyer les modifications locales vers le depot distant, on utilise "git push origin nom_de_branche"


pour recuperer les modifications du depot distant, on utilise "git pull origin nom_de_branche"
pour cloner un depot distant, on utilise "git clone url_du_depot"