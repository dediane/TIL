# Commandes GIT

- $ **git init** permet d'initialiser un répo git en local  
- $ **git add nom_fichier** permet d'ajouter nom_fichier à ton futur commit  
- $ **git commit** -m "message_commit" permet de faire un commit avec pour message message_commit  
- $ **git status** permet d'afficher l'état de tes fichiers par rapport au commit que tu es en train de réaliser (⚠ commande très pratique, à faire tout le temps)  
- $ **git diff nom_fichier** permet d'afficher les modifications de nom_fichier entre le dernier commit et le fichier actuel  
- $ **git log** permet d'afficher l'historique des commits  
- $ **git checkout SHA** permet de revenir en mode lecture uniquement au commit SHA  
- $ **git checkout master** permet de revenir au commit actuel  
- $ **git reset --hard SHA** permet de tout effacer pour revenir au commit SHA  
- $ **git reset --hard** permet de tout effacer pour revenir au dernier commit 
- $ **git revert SHA** permet d'annuler un commit 
- $ **git stash** permet de sauvegarder provisoirement son travail sans le commit  
- $ **git stash pop** permet de récupérer un travail précédemment sauvegardé avec git stash  
- $ **git remote -v** permet de voir les différentes remotes de ton repo git  
- $ **git remote add nom_remote url_remote** permet d'ajouter la remote url_remote à la liste de tes remotes. Cette remote aura le nom nom_remote (par convention, la remote principale où il y a le code s'appelle origin)  
- $ **git push nom_remote nom_branche** permet de pousser ta branche nom_branche vers ta remote nom_remote  
- $ **git pull nom_remote nom_branche** permet de récupérer ta branche nom_branche de ta remote nom_remote  
- $ **git ls -files** permet de voir la liste de fichiers sur le repo git  
- $ **git checkout .** si tu es un commit behind "origin", prends pas en compte les modifications que tu n'as pas commit -> ensuite on peut faire le git pull pour être au même niveau   
- $ **git --set-upstream**  set le repo github en remote lorsque on le crée grace à gh cli
- $ **git branch nom_branche** creer une branch 
- $ **git checkout nom_branche** se positionner sur la branche




# Exemple de workflow 


### CREER UNE NOUVELLE FEATURE:
- **git checkout development** 
- **git pull origin development**
- **git checkout -b feature/test** 

### PUSH SUR LA FEATURE:
- **git status** -> Vérifier que les modifications sont reliés à votre feature, sinon suprimer les modifications (éventuellement les sauvegarder pour les reporter sur une autre feature)
- **git add ...**  les fichiers un à un ( git add . autorisé au premier commit et les grosses modifs liées à un feature )
- **git commit -m "votre commentaire"**
- Premier push de la feature: **git push --set-upstream origin feature/test**
- Push suivants de la feature: **git push** -> Push de la feature sur le serveur

### MERGE LA FEATURE AVEC LE DEVELOPMENT:
- **git checkout development
- git pull origin development
- git checkout - 
- git merge development
- git checkout development 
- git merge feature/test
- git checkout - 
- git push** -> Push de la feature avec les merges sur le serveur

GERER ET INTEGRER UNE PULL REQUEST:
- Créer une Pull Request (PR)
- Demander à un membre du groupe de :
- Vérifier, valider la review et merge la PR
- Ne pas suprimer la branche de la feature
