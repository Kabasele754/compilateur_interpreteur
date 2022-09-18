dans lesquels tout est objet).

Dans ces langages, tous les objets font partie d'une même "classe" (au sens de la théorie des ensembles de Zermelo-Fraenkel), que l'on peut assimiler au type Object de Java. Chaque classe définit un sous-ensemble de ce type. Définir une classe B comme sous-classe de A revient à définir l'ensemble des objets de type B comme un sous-ensemble de l'ensemble des objets de type A.

Une fois ces concepts acquis, il devient logique de comprendre que si B hérite de A, alors une variable a de type A peut contenir une donnée de type B,mais qu'une variable b de type B ne peut a priori pas contenir une donnée de type A.

Ainsi, le code suivant est correct :

  //La classe B hérite de A
  A a;
  B b;
  ...
  a = b;
Mais le code qui suit est erroné :

  //La classe B hérite de A
  A a;
  B b;
  ...
  b = a;


# compilateur et  interpreteur

# Introduction

# Qu’est-ce qu’un compilateur ?

• C’est un programme qui reçoit en entrée un texte écrit 
dans un langage source (S) et produit en sortie un texte 
écrit dans un langage cible (C).

• Le compilateur traduit le texte source vers le texte cible

• Le compilateur est écrit dans un langage quelconque (L)

Si le texte cible est un programme exécutable, il peut être 
démarré

• Les données reçues en entrées (E) sont transformées par 
le texte cible pour produire les résultats (R)

# image

• Il y a donc trois langages impliqués dans la conception 
d’un compilateur

• Le langage source, qui peut être simple ou complexe

• Le langage cible, qui peut être simple ou complexe

• Le langage utilisé pour écrire le compilateur

• Il n’est pas obligatoire pour le compilateur d’écrire le code 
cible dans le langage de la machine.

• Quel langage devrait être utilisé pour écrire le 
compilateur?

• Comment était écrit le premier compilateur puisqu’il n’y 
avait pas de compilateur pour compiler ce compilateur?

• Problème de l’œuf et de la poule!

• Habituellement, la première version du compilateur est écrite 
avec un langage existant pour une sous-partie du langage 
source

• On peut ensuite réécrire le compilateur avec la partie 
supportée du langage, et utiliser le premier compilateur pour 
compiler le second

• On recommence une itération pour ajouter des fonctionnalités 
au langage

• Il est possible que la création d’un programme exécutable 
requière plusieurs autres programmes qu’un compilateur 
pour transformer le code source en programme

# Qu’est-ce qu’un interpréteur ?

• C’est un programme qui reçoit en entrée un texte écrit 
dans un langage source (S), ainsi que les entrées 
requises par le programme (E) et produit en sortie les 
résultats du texte d’entrée (R)

• L’interpréteur lit chacune des instructions indiquées dans 
le texte d’entrée et exécute les instructions appropriées 
sur la machine cible

# image

# Qu’est-ce qu’un compilateur hybride ?

• C’est une approche qui combine le compilateur et 
l’interpréteur

• Le texte source est transformé en code intermédiaire (I) 
qui peut être lu et exécuté par l’interpréteur à l’aide des 
données en entrée

• L’interpréteur produit les résultats finaux

# image

• Les avantages d’un compilateur hybride sont

• Grande portabilité du code

• Habituellement, une meilleure gestion des erreurs

• Les désavantages sont

• Souvent une vitesse d’exécution plus lente

• Les désavantages sont


• Un compilateur produit habituellement du code plus 

rapide qu’un interpréteur

• Le code produit par un compilateur est adapté à une 
machine en particulier. Le code est donc difficilement 
portable

• Souvent une vitesse d’exécution plus lente

• L’interprète est habituellement écrit dans un langage de 
haut niveau, il est donc plus portable.

• L’écriture d’un interpréteur demande habituellement 
moins de travail qu’un compilateur standard

• L’interpréteur travaille directement avec la représentation 
sémantique, ce qui améliore la sécurité et la gestion des 
erreurs
