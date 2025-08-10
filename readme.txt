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

pour envoyer les modifications locales vers le depot distant, on utilise "git push -u origin nom_de_branche"
exemple : "git push -u origin main" , 
faut s'assurer que la branche principale s'appelle "main" et pas "master"
Vérifiez le nom de votre branche actuelle dans le depot local : git branch
Si elle s'appelle master, renommez-la : git branch -M main
Poussez vers GitHub : git push -u origin main


pour recuperer les modifications du depot distant, on utilise "git pull origin nom_de_branche"
pour cloner un depot distant, on utilise "git clone url_du_depot"

# gestion des branches dans les depots distants
pour afficher les branches dans le depot local ou distantes, on utilise "git branch -a"
les branches distantes sont precedees de "remotes/"

NB : on push des branches et leur contenus vers le depot distant
exemple : "git push -u origin develop" pousse uniquement la branche develop
et son contenu vers le depot distant
C'est tout à fait normal et cela illustre une logique fondamentale de Git : 
pousser une branche ne pousse que l'histoire de cette branche, pas les autres branches elles-mêmes.
rappel : l'histoire du manuscrit final 
le resultat : L'éditeur a bien le livre final, mais il n'a pas reçu votre 
pile de carnets de notes (branch : develop) et de brouillons (branch : carnet_notes). 
Ces "étiquettes" de branches restent sur votre bureau (votre dépôt local) 
jusqu'à ce que vous décidiez de les envoyer explicitement.
ce qui est important pour l'éditeur étant le manuscrit final 
(la branche principale, souvent appelée "main" ou "master"),
vous n'avez pas besoin de lui envoyer les brouillons ou les notes de travail.

pour push une branche, on se deplace sur la branch en local avant de la push
exemple : "git checkout develop" avant de "git push -u origin develop"
la branche develop est creer dans le depot distant avec les connexion tel dans le depot local

NB: Si vous souhaitez que vos autres branches soient visibles sur le dépôt distant, 
vous devez les pousser explicitement. Au mieux branche par branche.

pour pouuser toutes les branches locales vers le depot distant, on utilise "git push --all origin"
NB : cette action n'est pas recommandee, car elle pousse toutes les branches locales

