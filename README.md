# Typologie des langages de programmation

## I. Introduction
Il existe des milliers de langages de programmation. On considère d'ailleurs que plus de 1500 langages sont utilisés à relativement large échelle de par le monde. Il existe de nombreuses raisons justifiant l'apparition de nouveaux langages, et le choix de tel ou tel langage pour répondre à un problème.

Dans la suite de ce document, quelques grands critères permettant de comparer les langages de programmation sont présentés.

## II. Paradigmes fondamentaux du langage
On appelle paradigme de programmation la façon dont on envisage l'exécution d'un programme. On distingue souvent 3 paradigmes principaux de programmation

### Programmation impérative
La programmation impérative est une programmation dans laquelle un programme est fait d'instructions dont l'exécution modifie l'état du programme. C'est le paradigme sous-jacent à la plupart des langages de programmation. Même si la plupart des langages impératifs sont des langages où les instructions sont exécutées séquentiellement, ce n'est nullement une obligation ; par exemple, dans un langage comme ADA, on peut spécifier que des instructions seront exécutées en parallèle. Les premiers langages de programmation étaient des langages impératifs. De nombreux langages récents sont également des langages impératifs.

Quelques exemples : C, Python, Java, Ada, Javascript

### Programmation fonctionnelle
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


## II. Paradigmes fondamentaux du langage
On appelle paradigme de programmation la façon dont on envisage l'exécution d'un programme. On distingue souvent 3 paradigmes principaux de programmation

### Programmation impérative
La programmation impérative est une programmation dans laquelle un programme est fait d'instructions dont l'exécution modifie l'état du programme. C'est le paradigme sous-jacent à la plupart des langages de programmation. Même si la plupart des langages impératifs sont des langages où les instructions sont exécutées séquentiellement, ce n'est nullement une obligation ; par exemple, dans un langage comme ADA, on peut spécifier que des instructions seront exécutées en parallèle. Les premiers langages de programmation étaient des langages impératifs. De nombreux langages récents sont également des langages impératifs.

Quelques exemples : C, Python, Java, Ada, Javascript

### Programmation fonctionnelle
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

### Programmation logique

La programmation logique est une programmation déclarative dans laquelle un problème va être décrit par des faits et des règles logiques. La résolution du problème consistera à trouver des valeurs satisfaisantes pour les valeurs inconnues en utilsant essentiellement 2 mécanismes : l'unification et le back-tracking (retour en arrière dans le cas de la récursivité). Les langages logiques sont en général réservés à la résolution de problèmes, et donc à l'intelligence artificielle. Le langage principal mettant en oeuvre ce paradigme est le langage Prolog, créé à Marseille par Alain Colmerauer en 1972.
```
# Exemple de programme en Prolog
# lancer swipl puis taper [peano].

entier(0).
entier(s(N)):- entier(N).

addition(N, 0, N).
addition(s(NM), s(N), M):-addition(NM, N,M).

multiplication(0, 0, _).
multiplication(Produit, s(N), M):- multiplication(ProdNM, N, M), addition(Produit, M, ProdNM).

conversion(0,0).
conversion(Entier,s(P)):- conversion(EntierP, P), Entier is EntierP+1.
```


## III. Paradigmes secondaires
Certaines autres caractéristiques des langages de programmation sont quelques fois considérés comme des paradigmes. En voici quelques-uns :

### Programmation orientée objets
Les langages orientés objets sont des langages dans lesquels les structures de données définissent aussi les traitements qui s'y rattachent. Si la plupart des langages orientés objets sont des langages de classe, certains reposent sur d'autres modèles, comme Javascript, qui est un langage à prototype.

La plupart des langages orientés objets sont des langages impératifs, mais OCAML (extension de CAML), par exemple, est un langage fonctionnel orienté objets

### Programmation événementielle
La programmation événementielle est un style de programmation qui consiste à déclencher des traitements lorsque des événements (externes ou générés par d'autres parties du programme) surviennent. C'est un style de programmation souvent utilisé dans le développement d'interfaces graphiques (entre autres dans le développement de documents Web). C'est aussi la base du fonctionnement d'un langage comme Scratch par exemple.

### Programmation orientée aspect
La programmation orientée aspect consiste à spécifier isolément certains aspects transverses au code métier afin d'éviter de le disséminer dans tous les fichiers source. Du coup, un "tisseur" d'aspects (programme qui ré-introduit ensuite les aspects aux bons endroits dans le code source avant compilation ou exécution) est nécessaire.

IV. Classification selon le code exécuté
Selon les langages, le code source peut être interprété directement lors de l'exécution, ou bien ce peut être une traduction de ce code source dans un autre langage qui est exécutée.

Langage interprété
Un langage interprété est un langage dont le code exécuté est le code source. Comme celui-ci n'est en général pas compréhensible par la machine, un interprète doit jouer le rôle de traducteur à la volée pour chaque exécution du programme. Un langage interprété est en général d'utilisation aisée, mais est lent à l'exécution, gourmand en ressources, et laisse souvent subsister des bugs.

Quelques exemples :

Python

Javascript

PHP

Lisp

### Langage compilé
Un langage compilé est un langage dont le code source est traduit une fois pour toute dans le langage du micro-processeur (langage machine) par un programme appelé compilateur. Le fichier ainsi produit est souvent appelé "code objet". L'utilisation d'un langage compilé est a priori moins facile que celle d'un langage interprété, puisque la phase de compilation est indispensable entre une modification du programme et son exécution. Il y a cependant 2 avantages essentiels par rapport aux langages interprétés :

le compilateur doit effectuer une analyse lexicale et syntaxique de tout le code source avant la compilation, ce qui permet d'enlever un certain nombre de bugs ;
l'exécution est beaucoup plus rapide.
Quelques exemples :


Quelques exemples :

C

Pascal

Eiffel
### Langage semi-compilé
Un langage semi-compilé est un langage dont le code source doit être traduit par un compilateur dans un code intermédiaire, proche du langage machine, appelé souvent byte code. Pour l'exécution, un interprèteur doit exécuter ce code intermédiaire.

### Compilation Juste à temps (JIT)
De plus en plus de langages interprétés ou semi-compilés proposent des compilations "juste à temps" : à l'exécution, si l'interprèteur détecte qu'un morceau du code est beaucoup utilisé, il peut dynamiquement compilé ce morceau là afin que les exécutions ultérieures soient beaucoup plus rapides. Cette pratique est notamment mise en oeuvre dans des langages comme Python ou Java.

## V. Niveau du langage
Il est également possible de classé les langages selon leur "niveau" : plus un langage est de haut niveau, plus il est éloigné de l'architecture matériel.

### Langage de bas niveau

Font partie de cette catégorie les assembleurs : ce sont des langages qui permettent juste de simplifier l'utilisation du langage machine : on utilise des mots-clés pour les instructions plutôt qu'un code hexadécimal, et on peut utiliser des étiquettes pour éviter des calculs d'adresse

### Langage intermédaire
On considère un langage comme un langage intermédiaire si celui-ci présente des structures de contrôle de plutôt haut niveau mais que malgré tout, la représentation en machine des données et du programme doivent être relativement bien connues pour pouvoir maîtriser le langage.

Le langage C est un exemple typique de langage intermédiaire.

### Langage de haut niveau
Les langages de haut niveau constitue la majeure partie des langages de programmation. Python, Java, Javascript, etc. font partie de cette catégorie.

Le code intermédiaire étant très proche d'un langage machine, son interprétation est très rapide. L'exécution est donc bien plus rapide que celle d'un langage interprété. Par ailleurs, le code intermédiaire est générique, donc la compilation ne doit pas être faite pour chaque architecture cible.

La notion de bytecode est apparue en 1972. Le langage qui a commencé à la populariser est sans nul doute le langage Java.

### Langage de 4ème génération
Les langages de quatrième génération sont des langages proposés par une application pour permettre d'automatiser des traitements de l'application. VBA en est un exemple.
## VI. Langage et typage
### A. Du typage strict au typage faible
#### 1. Les différentes catégories de typage
Un langage de programmation manipule des données. Ces données sont des valeurs d'un certain type. D'une façon plus formelle, on peut voir un type comme un ensemble et une valeur comme un élément de cette ensemble. Ainsi, quand un programme manipule la donnée "3.14", il s'agit d'un élément de l'ensemble des réels.

Dans un langage à typage strict, les types sont en fait des "classes" au sens de la théorie des ensembles de Zermelo-Fraenkel (et non au sens des langages à base de classes), ce qui signifie qu'ils sont disjoints et "non mélangeables" (ceci permet de rendre la théorie des ensembles consistante, en évitant par exemple le paradoxe de Russel). Par ailleurs, toute variable est aussi caractérisée par un type : une variable de type t ne peut contenir que des données de type t.

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
