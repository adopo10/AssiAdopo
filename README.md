# AssiAdopo
mon TP noté
https://github.com/adopo10/AssiAdopo.git
Dans ce projet, j'ai créé un système pour gérer la location de véhicules en utilisant les principes de la programmation orientée objet (POO). Les concepts clés que j'ai utilisés sont l'héritage, le polymorphisme et l'encapsulation, ainsi que la gestion des exceptions pour traiter les erreurs.

2. Héritage
L'héritage permet de définir des classes qui héritent des caractéristiques d'une autre classe. Dans mon système :

Classe Vehicule : J'ai conçu cette classe comme base, avec des attributs publics comme immatriculation, marque, modele, anneeMiseEnService, kilometrage, et statut.

Sous-classes Voiture et Camion : Ces classes héritent de Vehicule. La classe Voiture ajoute des attributs comme nombrePlaces et typeCarburant, tandis que Camion inclut capaciteChargement et nombreEssieux. Cela permet de partager le code commun tout en ajoutant des spécificités pour chaque type de véhicule.

3. Polymorphisme
Le polymorphisme permet d'utiliser une méthode de différentes manières selon le type d'objet. Dans mon projet :

Méthode calculerPrixLocation() : J'ai définie cette méthode dans Vehicule, puis je l'ai redéfinie dans Voiture et Camion. Cela permet d'avoir des calculs de prix différents selon le type de véhicule, tout en utilisant la même méthode.

Interface Louable : J'ai créé cette interface avec des méthodes comme louer() et retourner(). Les classes Voiture et Camion l'implémentent, ce qui permet d'utiliser le polymorphisme lors de la gestion des véhicules.

4. Encapsulation
L'encapsulation est importante pour protéger les données. Dans mon cas, j'ai utilisé des attributs publics pour faciliter l'accès, mais j'ai aussi créé des méthodes pour garantir une manipulation correcte des données.

Attributs publics : Tous les attributs de mes classes sont définis comme public, ce qui permet un accès direct, bien que cela puisse poser des problèmes d'intégrité des données.

Méthodes pour la logique : J'ai créé des méthodes comme louer() pour changer le statut d'un véhicule. Même si les attributs sont publics, ces méthodes permettent de contrôler les modifications.

5. Gestion des Exceptions
La gestion des exceptions est essentielle pour éviter les erreurs dans l'application. J'ai fait cela en :

Exceptions personnalisées : J'ai créé deux exceptions :

VehiculeIndisponibleException : Levée quand un client veut louer un véhicule qui est déjà loué.
ClientNonAutoriseException : Utilisée lorsque le client n'a pas le permis adéquat pour louer un camion.
Gestion des exceptions : Lors de la location d'un véhicule, je vérifie si le véhicule est disponible et si le client est autorisé. Si une erreur se produit, l'exception correspondante est levée, ce qui aide à gérer les problèmes efficacement.
