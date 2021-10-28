Ce fichier contient la liste des modifications/corrections prévues dans ce code. Ce fichier doit rester interne et ne pas se retrouver sur le github.  

#Tags :
- [#interface] : modification concernant l'interface utilisateur : la visualisation, les boutons, etc
- [#bug] : bogue
	- [#firefox] : bogue lié uniquement à firefox
- [#feature] : nouvelle fonctionnalité / complément à une fonctionnalité existante
- [#doc] : besoin en documentation


# AFAIRE :
- [ ] [#doc] mise à jour de la procédure de livraison : idem elements
- [ ] [#doc] ajouter un test d'import/export dans la procédure avant livraison
- [ ] [#interface] quand on importe, il faudrait une boite de dialogue pour demander si on veut fusionner avec la base existante ou créer une nouvelle (actuellement, si on sélectionne une tâche il ajoute les imports avec des '-1', si on est sur "new task" il fusionne)
- [x] [#feature] ajout d'un textfield comme choix, en plus des checkbox et dropdown
- [ ] [#bogue] segmentation : mes modifs union/substract ne fonctionnent pas dans l'app
- [ ] [#bogue] l'affichage n'est pas le même (boutons manquants) quand on appuie sur le bouton image dans la liste par rapport à un appui sur les "start *"
- [ ] [#feature] possibilité pour l’annotateur de passer à l’image suivante sans la valider (abandon)
- [ ] [#interface] quand on a l'interface sombre, les properties ne ressortent pas => il faudrait les mettre sur un fond coloré ou blanc ou alotrs modifier leur couleur : blanc si fond sombre par ex.
- [-] [#bogue #firefox] les propriétés sous forme de checkbox ne fonctionnent pas (uniquement sous firefox) :
	- ils reprennent la valeur par défaut si on passe à une annotation de classe différente puis qu'on y revient
	- si on modifie la valeur sur une boite, c'est propagé à toutes les autres boites de même classe sur lesquelles on clique
- [-] [#bogue #firefox] quand on édite les annotations, puis qu'on crée de nouveau sur la même image, les propriétés restent celles de la dernière annotation modifiée (et on la modifie donc) (uniquement sous firefox)
- [ ] [#bogue] pour modifier une tâche il faut créer une nouvelle tâche, puis revenir dessus... Action à déterminer
- [o] [#feature] affichage sous forme d’imagettes plutôt qu’une liste
	- [x] [#feature] création des imagettes et intégration dans la liste de fichiers
	- [ ] [#feature] généralisation des imagettes à toutes les formes de fichiers en entrée
- [ ] [#feature] affichage sous forme d'un mur d'imagette + étiquetage rapide directement sur le mur
	- possibilité de n'afficher dans ce mur qu'une sous-sélection grâce aux filtres dans la liste
- [ ] [#bogue] le REJECT ne fonctionne pas (firefox sur rectangle sans annotation dans l'image)
- [ ] [#bogue] après une sélection via un filtre, on reste sur la même page d'affichage, mais s'il n'y a plus autant d'images à afficher => il faudrait revenir à 0
- [ ] [#bogue] quand on clique sur l'affichage d'image après avoir filtré une partie du contenu, il ne fait rien (image vide ou image précédente s'il y en avait une
- [ ] [#feature] possibilité de prendre en compte une modification de la base de données images => bouton "refresh database" ?

- [ ] [#feature] revoir les rôles :
	- [ ] [#feature] possibilité d'utiliser des annotations multiples et concurrente et valider par consensus plutôt que d'avoir un validateur
	- [ ] [#feature] séparation complète des tâches d'admin qui ne devrait ni annoter, ni valider
	- [ ] [#feature] annotateurs à compétence différenciée, par ex : les annotateurs de niveau 1 font les BB autour des voitures, les annotateurs de niveau 2 complètent les marques et modèles

- [ ] [#feature] avoir des tags test/train/validation et pouvoir segmenter la base en fonction (en lien avec l’intégration de Semfeat ?)
- [ ] [#feature] intégration Semfeat/Élise

- [ ] [#interface] à la création d'une nouvelle tâche, il faudrait pouvoir décider si on souhaite étiqueter en mode shuffle (par défaut) ou linéaire (en suivant le nom des fichiers)
- [ ] [#interface] add an error message when creating task/dataset in a path which does not exist


- points à valider :
	- [ ] [#feature] possibilité de ne pas annoter tous les keypoints (non visibles) ?
	- [ ] [#feature] commencer par mettre les images en visu et ne plus mettre nécessairement toutes les images en to_annotate par défaut => il faut pouvoir sélectionner une partie de la base de donnée facilement pour l'étiquetage
	- [ ] [#feature] possibilité de sélectionner plusieurs éléments pour leur donner des caractéristiques communes ?
	- [ ] [#feature] passerelle Mturk / Amazon SageMaker
