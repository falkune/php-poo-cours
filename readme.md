# POO - programmation orientée objet

### Introduction à la POO 
La Programmation Orientée Objet (POO) est un paradigme de programmation qui permet de structurer son code de manière à le rendre plus modulaire, réutilisable et facile à maintenir. En PHP, la POO est une approche puissante qui offre de nombreux avantages pour le développement d'applications web et la gestion de projets complexes.

1) **Concepts de base de la POO :**

- **Objets :** En POO, un objet est une instance d'une classe. Il représente une entité qui possède des propriétés (attributs) et des comportements (méthodes).

- **Classes :** Une classe est un modèle ou un plan à partir duquel les objets sont créés. Elle définit la structure et le comportement des objets.

- **Encapsulation :** L'encapsulation consiste à regrouper les données et les méthodes qui les manipulent au sein d'une même entité, appelée objet. Cela permet de restreindre l'accès aux données et de garantir leur intégrité.

- **Héritage :** Le mécanisme d'héritage permet à une classe (appelée classe fille) d'hériter des propriétés et des méthodes d'une autre classe (appelée classe parent), favorisant ainsi la réutilisation du code et la construction de hiérarchies.

- **Polymorphisme :** Le polymorphisme permet à des objets de différentes classes de répondre de manière spécifique à des messages ou des appels de méthodes, offrant ainsi une grande flexibilité dans la conception et l'utilisation des objets.

2) **Avantages de la POO :**

- **Modularité :** La POO favorise la création de modules autonomes, facilitant ainsi la maintenance et l'évolutivité du code.

- **Réutilisabilité :** Grâce à l'héritage et à la composition, les classes et les objets peuvent être réutilisés dans différentes parties de l'application.

- **Abstraction :** La POO permet de représenter des concepts du monde réel sous forme d'objets, facilitant ainsi la compréhension et la gestion du code.

- **Encapsulation et sécurité :** En encapsulant les données et en définissant des niveaux d'accès appropriés, la POO garantit l'intégrité des données et réduit les risques de modification accidentelle.

- **Maintenabilité :** La structure modulaire et organisée de la POO rend le code plus facile à comprendre, à tester et à mettre à jour.

En résumé, la POO en PHP offre un ensemble de concepts et de pratiques permettant de développer des applications robustes, flexibles et évolutives. Dans ce cours, nous explorerons en détail ces concepts fondamentaux ainsi que leur mise en œuvre pratique dans le langage PHP.

### Les classes en PHP
Les classes en PHP sont des structures fondamentales de la programmation orientée objet (POO). Elles permettent de définir des modèles à partir desquels des objets peuvent être créés. Voici une explication détaillée des différents aspects des classes en PHP :

1) **Définition d'une classe :**
En PHP, une classe est définie à l'aide du mot-clé class, suivi du nom de la classe. Par exemple :

```php
class MaClasse {
    // Corps de la classe
}
```
2) **Propriétés (attributs) :**
Les propriétés, également appelées attributs, sont des variables qui définissent les caractéristiques d'un objet. Elles représentent l'état de l'objet. Les propriétés sont déclarées à l'intérieur de la classe. Par exemple :

```php
class Voiture {
    public $marque;
    public $modele;
    public $annee;
}
```

3) **Méthodes :**
Les méthodes sont des fonctions définies à l'intérieur d'une classe. Elles définissent le comportement des objets de cette classe. Par exemple :

```php
class Voiture {
    public function demarrer() {
        // Code pour démarrer la voiture
    }

    public function arreter() {
        // Code pour arrêter la voiture
    }
}
```

4) **Visibilité des membres :**
En PHP, les propriétés et les méthodes peuvent avoir différents niveaux de visibilité :
- *public* : accessible depuis n'importe où.
- *private* : accessible uniquement depuis l'intérieur de la classe.
- *protected* : accessible depuis la classe elle-même et ses classes dérivées (héritage).

5) **Méthodes magiques :**
PHP fournit des méthodes magiques qui sont automatiquement appelées dans des situations spécifiques. Par exemple, __construct est appelée lors de l'instanciation d'un objet, __destruct lors de sa destruction, etc.

```php
class MaClasse {
    public function __construct() {
        // Code exécuté lors de l'instanciation de l'objet
    }

    public function __destruct() {
        // Code exécuté lors de la destruction de l'objet
    }
}
```

En conclusion, les classes en PHP sont des structures qui permettent de modéliser des entités et des comportements dans le cadre de la programmation orientée objet. Elles constituent le fondement de la création d'objets et de la mise en œuvre de concepts tels que l'encapsulation, l'héritage et le polymorphisme.

### L'instanciation d'objets
L'instanciation d'objets en PHP est le processus de création d'une instance d'une classe. Cela implique de créer un objet basé sur le modèle défini par la classe. Voici comment cela fonctionne en pratique :

1) **Création d'un objet :**
Pour instancier un objet en PHP, utilisez le mot-clé new suivi du nom de la classe, suivi éventuellement de parenthèses si la classe a un constructeur sans paramètres. Par exemple :

```php
$voiture = new Voiture();
```
Cette ligne de code crée un nouvel objet de la classe Voiture et le stocke dans la variable *$voiture*.

2) **Utilisation des objets :**
Une fois l'objet créé, vous pouvez accéder à ses propriétés et méthodes à l'aide de l'opérateur de sélection **->**. Par exemple, pour accéder à la propriété marque de l'objet *$voiture*, vous pouvez faire :

```php
$voiture->marque = "Toyota";
```
Vous pouvez également appeler des méthodes sur l'objet, par exemple :

```php
$voiture->demarrer();
```

3) **Destruction d'objets :**
En PHP, la mémoire utilisée par les objets n'est pas automatiquement libérée lorsque vous avez fini de les utiliser. Vous pouvez toutefois détruire explicitement un objet en utilisant le mot-clé *unset*, par exemple :

```php
unset($voiture);
```

Cela détruira l'objet $voiture et libérera la mémoire qu'il occupait.

En résumé, l'instanciation d'objets en PHP consiste à créer des instances de classes à l'aide du mot-clé new, ce qui vous permet d'accéder aux propriétés et méthodes définies dans la classe. Une fois que vous avez fini d'utiliser un objet, vous pouvez le détruire explicitement à l'aide de unset.

### L'encapsulation

L'encapsulation est l'un des principes fondamentaux de la programmation orientée objet (POO) qui consiste à regrouper les données (propriétés ou attributs) et les méthodes (fonctions ou comportements) qui les manipulent au sein d'une même entité, appelée objet. En PHP, l'encapsulation est mise en œuvre à l'aide des niveaux de visibilité des membres de classe : public, private et protected.

Voici une explication détaillée de chaque niveau de visibilité et de son rôle dans l'encapsulation :

1) **Public :**
- Les membres de classe déclarés comme public sont accessibles depuis n'importe où en dehors de la classe.
- Ils peuvent être modifiés et accédés directement depuis n'importe quel endroit du code.
- Cependant, l'utilisation excessive de membres publics peut compromettre l'encapsulation en exposant l'état interne de l'objet.

```php
class Voiture {
    public $marque;
    public $modele;

    public function demarrer() {
        echo "La voiture démarre.";
    }
}
```

2) **Private :**
- Les membres de classe déclarés comme private sont accessibles uniquement à l'intérieur de la classe où ils sont définis.
- Ils ne peuvent pas être accédés ou modifiés depuis l'extérieur de la classe.
- L'encapsulation est renforcée car l'état interne de l'objet est caché aux autres parties du code.

```php
class Voiture {
    private $vitesse;

    public function accelerer($vitesse) {
        $this->vitesse += $vitesse;
    }
}
```

3) **Protected :**
- Les membres de classe déclarés comme protected sont similaires aux membres private, mais ils sont également accessibles à partir des classes enfants (héritage).
- Ils ne peuvent pas être accédés ou modifiés depuis l'extérieur de la classe, sauf par les classes enfants.

En résumé, l'encapsulation en PHP permet de cacher les détails d'implémentation d'une classe et de protéger ses données contre les accès non autorisés.

### Utilisation des getters et setters
Les getters et setters sont des méthodes utilisées dans la programmation orientée objet pour accéder et modifier les propriétés d'un objet de manière contrôlée. En PHP, ils sont souvent utilisés pour assurer l'encapsulation des données en permettant un accès sécurisé aux propriétés privées ou protégées d'une classe.

1) **Getters :**
Les getters sont des méthodes utilisées pour récupérer la valeur d'une propriété d'un objet. Ils permettent d'accéder à des propriétés privées ou protégées depuis l'extérieur de la classe.Exemple :

```php
class Personne {
    private $nom;

    public function getNom() {
        return $this->nom;
    }
}

// Utilisation du getter pour accéder à la propriété privée
$personne = new Personne();
echo $personne->getNom(); // Affiche le nom de la personne
```

2) **Setters :**
Les setters sont des méthodes utilisées pour modifier la valeur d'une propriété d'un objet. Ils permettent de définir des contrôles et des validations lors de la modification d'une propriété.Exemple de setter en PHP :

```php
class Personne {
    private $nom;

    public function setNom($nouveauNom) {
        // Ajouter des validations si nécessaire
        $this->nom = $nouveauNom;
    }
}

// Utilisation du setter pour modifier la propriété privée
$personne = new Personne();
$personne->setNom("John Doe"); // Définit le nom de la personne
```

En utilisant des getters et des setters, vous pouvez contrôler l'accès aux propriétés d'une classe, ce qui améliore la sécurité et la cohérence de votre code. De plus, cela vous permet de mettre en place des validations et des logiques spécifiques lors de la récupération ou de la modification des données, ce qui rend votre code plus robuste et plus flexible.

### L'héritage
L'héritage est un concept clé de la programmation orientée objet (POO) qui permet à une classe (appelée classe fille ou sous-classe) de hériter des propriétés et des méthodes d'une autre classe (appelée classe parent ou superclasse). Cela permet de créer une relation de spécialisation entre les classes, où la classe fille hérite du comportement et des caractéristiques de la classe parent, tout en ayant la possibilité de définir ses propres méthodes et propriétés spécifiques.

En PHP, l'héritage est défini à l'aide du mot-clé extends. Voici comment cela fonctionne :

```php
// Classe parent
class Animal {
    protected $nom;
    protected $age;

    public function __construct($nom, $age) {
        $this->nom = $nom;
        $this->age = $age;
    }

    public function manger() {
        echo "Je mange.";
    }
}

// Classe fille Chien
class Chien extends Animal {
    private $race;

    public function __construct($nom, $age, $race) {
        parent::__construct($nom, $age);
        $this->race = $race;
    }

    public function aboie() {
        echo "Woof!";
    }
}

// Classe fille Chat
class Chat extends Animal {
    private $couleur;

    public function __construct($nom, $age, $couleur) {
        parent::__construct($nom, $age);
        $this->couleur = $couleur;
    }

    public function miaule() {
        echo "Meow!";
    }
}

// Utilisation de l'héritage
$chien = new Chien("Rex", 3, "Labrador");
$chat = new Chat("Felix", 2, "Noir");

echo $chien->aboie(); // Affiche "Woof!"
echo $chat->miaule(); // Affiche "Meow!"

echo $chien->manger(); // Affiche "Je mange."
echo $chat->manger(); // Affiche "Je mange."
```

### Le polymorphisme
Le polymorphisme est un concept fondamental de la programmation orientée objet (POO) qui permet à des objets de différentes classes de répondre de manière spécifique à des appels de méthodes identiques. En d'autres termes, le polymorphisme permet à des objets de différentes classes d'avoir une interface commune mais de comportements différents.

En PHP, le polymorphisme est souvent réalisé à travers l'héritage et l'implémentation d'interfaces. Voici comment cela fonctionne :

1) **Polymorphisme par héritage :**
Avec l'héritage, une classe fille peut hériter des méthodes de sa classe parent et les redéfinir si nécessaire. Cela permet à différentes classes d'avoir des comportements différents pour une même méthode.Exemple :

```php
// Classe parent
class Animal {
    public function sePresenter() {
        echo "Je suis un animal.";
    }
}

// Classe fille Chien
class Chien extends Animal {
    public function sePresenter() {
        echo "Je suis un chien et je fais Woof!";
    }
}

// Classe fille Chat
class Chat extends Animal {
    public function sePresenter() {
        echo "Je suis un chat et je fais Meow!";
    }
}

// Utilisation du polymorphisme
$chien = new Chien();
$chat = new Chat();

$chien->sePresenter(); // Affiche "Je suis un chien et je fais Woof!"
$chat->sePresenter(); // Affiche "Je suis un chat et je fais Meow!"
```

2) **Polymorphisme par interfaces :**
Les interfaces définissent un contrat que les classes doivent respecter en implémentant les méthodes de l'interface. Cela permet à différentes classes d'avoir des implémentations différentes pour une même méthode, mais avec une interface commune.Exemple :

```php
// Interface
interface Animal {
    public function sePresenter();
}

// Classe Chien
class Chien implements Animal {
    public function sePresenter() {
        echo "Je suis un chien et je fais Woof!";
    }
}

// Classe Chat
class Chat implements Animal {
    public function sePresenter() {
        echo "Je suis un chat et je fais Meow!";
    }
}

// Utilisation du polymorphisme par interfaces
function presenterAnimal(Animal $animal) {
    $animal->sePresenter();
}

$chien = new Chien();
$chat = new Chat();

presenterAnimal($chien); // Affiche "Je suis un chien et je fais Woof!"
presenterAnimal($chat); // Affiche "Je suis un chat et je fais Meow!"
```

### Les espaces de noms (namespaces)
Les espaces de noms (ou namespaces en anglais) sont une fonctionnalité de PHP qui permet d'organiser et de structurer les classes, les fonctions et les constantes dans un espace de noms spécifique. Cela permet d'éviter les conflits de noms entre différentes parties d'une application PHP, en particulier lorsque vous travaillez avec des bibliothèques tierces ou de grands projets.

1) **Déclaration d'un espace de noms :**
Pour déclarer un espace de noms, utilisez le mot-clé namespace, suivi du nom de l'espace de noms. Cette déclaration doit être placée au début du fichier PHP, avant toute autre déclaration.Exemple :

```php
namespace MonProjet;

class MaClasse {
    // Contenu de la classe
}
```

2) **Utilisation des classes dans un espace de noms :**
Pour utiliser une classe définie dans un espace de noms, vous devez spécifier le nom complet de la classe en incluant le nom de l'espace de noms.Exemple :

```php
$objet = new MonProjet\MaClasse();
```
Autre exemple:

```php
<?php
# namespace1
namespace MonProjet\Namespace1;

class MaClasse {
    public function bonjour() {
        echo "Bonjour depuis MaClasse dans l'espace de noms Namespace1.";
    }
}

# namespace2
namespace MonProjet\Namespace2;

class MaClasse {
    public function bonjour() {
        echo "Bonjour depuis MaClasse dans l'espace de noms Namespace2.";
    }
}

# fichier principal
require_once 'namespace1/MaClasse.php';
require_once 'namespace2/MaClasse.php';

use MonProjet\Namespace1\MaClasse as MaClasse1;
use MonProjet\Namespace2\MaClasse as MaClasse2;

// Utilisation des classes
$objet1 = new MaClasse1();
$objet1->bonjour();

$objet2 = new MaClasse2();
$objet2->bonjour();
```

### Les traits (traits)
Les traits (traits en anglais) sont une fonctionnalité de la programmation orientée objet (POO) introduite dans PHP 5.4. Ils permettent la réutilisation de méthodes dans plusieurs classes de manière horizontale, c'est-à-dire sans utiliser l'héritage. Les traits offrent une alternative à l'héritage multiple en permettant à une classe d'inclure des méthodes à partir d'un ou plusieurs traits.

Voici comment utiliser les traits en PHP :

1) **Déclaration d'un trait :**
Pour déclarer un trait, utilisez le mot-clé trait, suivi du nom du trait. À l'intérieur du trait, vous pouvez définir des méthodes comme dans une classe normale.Exemple :

```php
trait MonTrait {
    public function direBonjour() {
        echo "Bonjour depuis MonTrait.";
    }
}
```

2) **Utilisation d'un trait dans une classe :**
Pour inclure un trait dans une classe, utilisez le mot-clé use suivi du nom du trait. Vous pouvez inclure plusieurs traits en les séparant par des virgules.Exemple :

```php
class MaClasse {
    use MonTrait;
}
```

3) **Utilisation de méthodes de trait :**
Une fois qu'un trait est utilisé dans une classe, les méthodes définies dans le trait deviennent disponibles pour cette classe comme si elles avaient été définies directement dans la classe.Exemple :

```php
$objet = new MaClasse();
$objet->direBonjour(); // Affiche "Bonjour depuis MonTrait."
```

4) **Conflict Resolution :**
En cas de conflit de noms entre les méthodes définies dans un trait et celles de la classe, vous pouvez utiliser l'aliasing de méthode pour résoudre le conflit.Exemple :

```php
trait MonTrait {
    public function direBonjour() {
        echo "Bonjour depuis MonTrait.";
    }
}

class MaClasse {
    use MonTrait {
        direBonjour as direSalut; // Alias de la méthode direBonjour
    }
}

$objet = new MaClasse();
$objet->direSalut(); // Affiche "Bonjour depuis MonTrait."
```
Les traits offrent une flexibilité supplémentaire dans la conception de classes en permettant la réutilisation de code sans les contraintes de l'héritage. Ils sont particulièrement utiles lorsque vous souhaitez partager du code entre plusieurs classes qui ne sont pas nécessairement liées par une hiérarchie d'héritage.

### Attributs et méthodes statiques
Les attributs et méthodes statiques sont des éléments de la programmation orientée objet (POO) qui sont partagés par toutes les instances d'une classe. Contrairement aux attributs et méthodes non statiques, les attributs et méthodes statiques sont associés à la classe elle-même plutôt qu'à ses instances individuelles. Cela signifie que vous pouvez accéder à ces attributs et méthodes sans avoir besoin d'instancier la classe.

Voici comment définir et utiliser des attributs et des méthodes statiques en PHP :

1) **Attributs statiques :**
Les attributs statiques sont déclarés à l'aide du mot-clé static et peuvent être accédés directement à partir de la classe, sans avoir besoin d'instancier la classe.Exemple :

```php
class MaClasse {
    public static $attributStatique = 0;
}

// Accès à l'attribut statique
echo MaClasse::$attributStatique;
```

2) **Méthodes statiques :**
Les méthodes statiques sont également déclarées à l'aide du mot-clé static. Elles peuvent être appelées directement à partir de la classe, sans avoir besoin d'instancier la classe.Exemple :

```php
class MaClasse {
    public static function maMethodeStatique() {
        echo "Ceci est une méthode statique.";
    }
}

// Appel de la méthode statique
MaClasse::maMethodeStatique();
```

3) **Utilisation :**
Les attributs et méthodes statiques peuvent être utilisés pour stocker des valeurs partagées entre toutes les instances de la classe, ou pour fournir des fonctionnalités utilitaires qui ne dépendent pas de l'état d'une instance particulière.Exemple :

```php
class Compteur {
    public static $compteur = 0;

    public static function incrementer() {
        self::$compteur++;
    }

    public static function afficherCompteur() {
        echo "Nombre d'instances créées : " . self::$compteur;
    }
}

// Utilisation
Compteur::incrementer();
Compteur::incrementer();
Compteur::afficherCompteur(); // Affiche "Nombre d'instances créées : 2"
```

Les attributs et méthodes statiques sont utiles lorsque vous avez besoin de partager des valeurs ou des fonctionnalités entre toutes les instances d'une classe, ou lorsque vous souhaitez fournir des fonctionnalités utilitaires qui ne sont pas spécifiques à une instance particulière. Cependant, l'abus des attributs et méthodes statiques peut rendre le code moins testable et plus difficile à maintenir, donc utilisez-les avec précaution.






