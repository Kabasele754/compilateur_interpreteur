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
