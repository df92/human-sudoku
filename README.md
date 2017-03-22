# huma-sudo
Simulation de joueur humain de sudoku

Projet développé en Python 3, entièrement en code objet. Il simule un joueur humain qui tente de résoudre une grille de Sudoku. Le programme n'utilise pas la force brute ni aucune optimisation algorithmique et ne cherche pas la rapidité. Au contraire il tente de reproduire fidèlement les contraintes et limites de l'homme pour ce jeu. 

Pour commencer, le joueur humain a beaucoup de limites cognitives (et il n'est pas "surdoué"). Il ne peut pas "connaître par coeur" toute la grille. Il doit l'observer de manière répétitive et intensive pour y chercher visuellement les informations parcellaires avec lesquelles il "réfléchit" . De même, le joueur a une "mémoire de travail" limitée, imparfaite, et éphémère. Il a toutes les chances d'avoir oublié un détail vu quelques minutes auparavant. Enfin, le joueur a une certaine intelligence qui lui permet de tenter d'appliquer des techniques de résolution "humaines", mais la limite de son intelligence l'empêche de faire des raisonnements complexes comme par exemple imbriquer trop de techniques entre elles. S'il essaie, il va tout mélanger en mémoire et aboutir à une confusion qui le fera échouer et le forcera à revenir à des techniques plus simples.

Il y a évidemment une limite de niveau car le programme ne simule pas la possibilité pour le joueur de noter (sur papier) des hypothèses. S'il fait un essai de valeur incertain, il doit donc se le rappeler. Dans la réalité à partir d'un certain niveau de grille, il faut soit une mémoire hors du commun, soit un bloc-note. Mais cette simulation pourrait être ajoutée au programme actuel.

A l'inverse, il y a une simulation d'intelligence. D'une part le programme reproduit des techniques de résolution simples (autrement dit des raisonnements logiques) et d'autre part il tente d'appliquer la bonne technique au bon moment. Par exemple il cherche des coups triviaux (ex: s'il reste une seule case libre dans un carré) et des opportunités apparues après un placement. S'il applique une technique qui ne donne rien, il va l'abandonner et en utiliser une autre.

Enfin le programme simule une capacité d'apprentissage grâce à du code de type réseau neuronal. Par conséquent des choses qui marchent bien seront préférées par la suitej

Le "niveau du joueur" est calibré par des profils de mémoire et d'intelligence qui tentent d'être des simulations réalistes. Il est donc tout-à-fait logique qu'un joueur échoue à résoudre une grille trop compliquée pour lui.

C'est un projet évolutif car il est toujours possible d'améliorer le réalisme de la simulation. Un bon exemple est la mémoire, car la mémoire humaine est associative d'une manière quasi-infinie. Cela est très difficile à simuler.

sur le plan des interfaces, le code de simulation est entièrement distinct de celui des E/S. Il est donc possible d'ajouter facilement des modes d'interface, par exemple fenêtrés. 
Dans la version actuelle les grilles sont lues comme des listes de chiffres (ou 0 représente une case vide). Il est donc possible et facile d'interfacer le programme avec des générateurs de grilles, ou d'utiliser des fichiers de format texte, Excel, etc.

Le code contient déjà des fonctions paramétrables de journalisation (log) des actions. Cela permet de suivre comment le programme a joué, et c'est aussi très utile pour tester et débugger.
