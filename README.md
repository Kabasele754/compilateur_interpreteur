# Typologie des langages de programmation

## I. Introduction
Il existe des milliers de langages de programmation. On considère d'ailleurs que plus de 1500 langages sont utilisés à relativement large échelle de par le monde. Il existe de nombreuses raisons justifiant l'apparition de nouveaux langages, et le choix de tel ou tel langage pour répondre à un problème.

Dans la suite de ce document, quelques grands critères permettant de comparer les langages de programmation sont présentés.

## II. Paradigmes fondamentaux du langage
On appelle paradigme de programmation la façon dont on envisage l'exécution d'un programme. On distingue souvent 3 paradigmes principaux de programmation

Programmation impérative
La programmation impérative est une programmation dans laquelle un programme est fait d'instructions dont l'exécution modifie l'état du programme. C'est le paradigme sous-jacent à la plupart des langages de programmation. Même si la plupart des langages impératifs sont des langages où les instructions sont exécutées séquentiellement, ce n'est nullement une obligation ; par exemple, dans un langage comme ADA, on peut spécifier que des instructions seront exécutées en parallèle. Les premiers langages de programmation étaient des langages impératifs. De nombreux langages récents sont également des langages impératifs.

Quelques exemples : C, Python, Java, Ada, Javascript

Programmation fonctionnelle
La programmation fonctionnelle est une programmation dans laquelle un programme est une composition de fonctions calculant un résultat à partir de données d'entrée. La théorie sous-jacente est celle du λ-calcul, introduite par Church en 1925. Le premier langage fonctionnel fut le Lisp (1958), qui eut un certain succès, notamment dans le domaine de l'IA. D'autres langages fonctionnels sont à citer :

ML (1970), plus proche de la théorie de λ-calcul ;
CAML (1985), déclinaison française de ML, autorisant la programmation impérative et objet ;
Haskell(1990), une version plus moderne, très pure, de la notion de langage fonctionnel.

```
-- Exemple de programme en Haskell
-- lancer ghci puis taper :load peano

data Peano = Zero | Succ Peano deriving Show

addition Zero x = x
addition (Succ entier1) entier2 = addition entier1 (Succ entier2)

(+.) Zero x = x
(+.) (Succ entier1) entier2 = entier1  +. (Succ entier2)

conversion Zero = 0
conversion (Succ entier) = 1 + conversion entier

multiplication Zero _ = Zero
multiplication (Succ entier1) entier2 = addition entier2 (multiplication entier1 entier2)

conv2 0 = Zero
conv2 x = Succ (conv2 (x-1))

```

Typologie des langages de programmation ↑ →
I. Introduction
Il existe des milliers de langages de programmation. On considère d'ailleurs que plus de 1500 langages sont utilisés à relativement large échelle de par le monde. Il existe de nombreuses raisons justifiant l'apparition de nouveaux langages, et le choix de tel ou tel langage pour répondre à un problème.

Dans la suite de ce document, quelques grands critères permettant de comparer les langages de programmation sont présentés.

II. Paradigmes fondamentaux du langage
On appelle paradigme de programmation la façon dont on envisage l'exécution d'un programme. On distingue souvent 3 paradigmes principaux de programmation

Programmation impérative
La programmation impérative est une programmation dans laquelle un programme est fait d'instructions dont l'exécution modifie l'état du programme. C'est le paradigme sous-jacent à la plupart des langages de programmation. Même si la plupart des langages impératifs sont des langages où les instructions sont exécutées séquentiellement, ce n'est nullement une obligation ; par exemple, dans un langage comme ADA, on peut spécifier que des instructions seront exécutées en parallèle. Les premiers langages de programmation étaient des langages impératifs. De nombreux langages récents sont également des langages impératifs.

Quelques exemples : C, Python, Java, Ada, Javascript

Programmation fonctionnelle
La programmation fonctionnelle est une programmation dans laquelle un programme est une composition de fonctions calculant un résultat à partir de données d'entrée. La théorie sous-jacente est celle du λ-calcul, introduite par Church en 1925. Le premier langage fonctionnel fut le Lisp (1958), qui eut un certain succès, notamment dans le domaine de l'IA. D'autres langages fonctionnels sont à citer :

ML (1970), plus proche de la théorie de λ-calcul ;
CAML (1985), déclinaison française de ML, autorisant la programmation impérative et objet ;
Haskell(1990), une version plus moderne, très pure, de la notion de langage fonctionnel.
-- Exemple de programme en Haskell
-- lancer ghci puis taper :load peano

data Peano = Zero | Succ Peano deriving Show

addition Zero x = x
addition (Succ entier1) entier2 = addition entier1 (Succ entier2)

(+.) Zero x = x
(+.) (Succ entier1) entier2 = entier1  +. (Succ entier2)

conversion Zero = 0
conversion (Succ entier) = 1 + conversion entier

multiplication Zero _ = Zero
multiplication (Succ entier1) entier2 = addition entier2 (multiplication entier1 entier2)

conv2 0 = Zero
conv2 x = Succ (conv2 (x-1))
Le paradigme fonctionnel a le vent en poupe : de nombreux langages récents intègrent des aspects fonctionnels, au sens où :

les fonctions sont des données comme les autres, qui peuvent donc être passées en paramètres à d'autres fonctions
il est possible de définir à la volée des fonctions anonymes appelées λ-expressions.
Parmi ces langages, on trouve notamment :

Skala

Java (à partir de Java 8)

Javascript

Python

Swift

## Programmation logique

La programmation logique est une programmation déclarative dans laquelle un problème va être décrit par des faits et des règles logiques. La résolution du problème consistera à trouver des valeurs satisfaisantes pour les valeurs inconnues en utilsant essentiellement 2 mécanismes : l'unification et le back-tracking (retour en arrière dans le cas de la récursivité). Les langages logiques sont en général réservés à la résolution de problèmes, et donc à l'intelligence artificielle. Le langage principal mettant en oeuvre ce paradigme est le langage Prolog, créé à Marseille par Alain Colmerauer en 1972.

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
