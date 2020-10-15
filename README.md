# Projet-POOIG

Ce projet est basé sur le jeu **Pet Rescue** Sagaque vous pouvez essayer gratuitement sur votre téléphone ou comme un jeu facebook. Vous avez probablement déjà passé du temps sur des jeux de ce type, et l’intérêt ici est devous rendre compte du travail à fournir pour en réaliser les bases. Bien entendu il ne s’agit pas deproduire un résultat final de qualité professionnelle, mais d’aborder le problème de sa conception en compartimentant bien les différents aspects, quitte à les améliorer ensuite.

# Implementation :

## Environnement de jeu :
  C’est l’endroit qui manipule les niveaux et la progression des joueurs. Vous avez l’occasion d’y faire l’accueil du joueur, d’y présenter les règles du jeu, ou de passer directement à des démonstrations précises pour gagner du temps lors de la soutenance. Idéalement à cette étape certains éléments seront sauvegardés ou importés du disque. Enjava les sauvegardes se font assez simplement en faisant en sorte que vos objets implémentent l’interface Serialisable. Référez vous à la documentation de cette interface.

## Le plateau :
   Les joueurs etcUne partie de votre modèle sera constitué d’un plateau de jeu. La nature de ce jeu fait quevous y aurez certainement défini un membre de type tableau ainsi que d’autres caractéristiques àdéfinir. Pensez par exemple que le jeu se déroule dans une section considérée visible de ce plateau.La réorganisation d’un plateau est propre aux plateaux, c’est dans cette classe qu’il vous faudraécrire les méthodes correspondantes.La façon dont les joueurs interagissent avec le plateau est à déterminer en anticipant lasignature des méthodes que vous souhaitez utiliser.

## Les phases du jeu en lui même :
  Il est toujours préférable d’avoir plusieurs petites méthodes à écrire plutôt qu’une seule grandeméthode qui ferait un travail compliqué à déchiffrer.Si vous avez quelque part dans votre code un bloc qui fait plus d’une vingtaine de lignes,alors il est quasi certain que vous devriez vous relire pour introduire une phase intermédiaire.

## Nature des joueurs :
  Si de prime abord on pense naturellement à un joueur humain, il n’est pas très difficile de lesubstituer par un joueur robot. Celui ci n’a pas besoin d’être très intelligent, mais il vous fautprévoir cette possibilité et l’illustrer. Toute l’intelligence se juge dans le choix des coups, maisvous pouvez vous contenter de prendre n’importe quel coup possible. (Dans une version plusévoluée vous pourriez prendre le coup qui fait disparaître le plus de cubes ou, dans une versionvraiment plus aboutie, chercher à anticiper quelle serait la situation à 3 ou 4 coups d’avance.Toute idée est ici la bienvenue)

## Vue et Modèle :
  Un point important est de bien séparer la vue du modèle. La vue désigne l’ensemble desaspects liés au rendu graphique, et le modèle regroupe l’ensemble des concepts qui sont sous-jacent, vraiment propres au jeu, et qui sont largement indépendant de la vue. Ainsi, si vous souhaitez faire évoluer votre programme pour en changer la présentation, par exemple pour l’adapter à l’écran d’un téléphone ou d’une tablette, alors l’essentiel du jeu seratout de même préservé. Les changements à faire relèvent tous de ce qu’on appelle la vue. De la même façon, si on souhaite changer un peu les règles, ajouter des variantes, celles ci concernent essentiellement le modèle. Dans votre cas, de toutes façons, vous allez dans un premier temps présenter les choses enmode texte puisque les aspects graphiques seront abordés progressivement en cours de semestre. Puis, lorsque vous serez plus avancé dans votre réflexion, que vous aurez davantage de connais-sances sur les interfaces graphiques, et que vous aurez mieux cerné ce que vous souhaitez apporter au projet, alors il sera temps de redéfinir les vues. Vous pouvez prévoir cela en définissant assez tôt une interface ou une classes abstraites pour les vues attendues, il suffira ensuite de l’instancier par des sous-classes plus ou moins évoluée (textuelle ou graphique). L’association entre les modèles et les vues se fera en introduisant un champs typé Vue Generale dans le modèle de votre jeu, et réciproquement si besoin. Pour rendre compte d’une modification, graphique outextuelle, le jeu s’adressera à sa vue. La vue se chargera aussi de transmettre les actions choisiespar le joueur au modèle.

## Options :
  Voici quelques propositions qui peuvent vous inspirer en particulier si au cours du dévelop-pement ou de la répartition des taches l’un d’entre vous a un peu plus de temps que l’autre.Il est possible de travailler à un éditeur de niveau (sommaire), de proposer la possibilité derevenir en arrière en annulant le dernier coup, de demander de l’aide en obtenant en retour unezoneintéressante à jouer(un concept algorithmique)

## Règle universelle :
  Organisez-vous pour avancer petit à petit, régulièrement, sans vous perdre complètement surles aspects graphiques.
