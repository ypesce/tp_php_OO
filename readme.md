#TP Php OO partie théorique
Question 1.
```php
  interface User {
    public function login($username, $password);
  } 
  class UserLogin implements User {
     public function login($username, $password) {
       
    }
  }
```

Question 2.

```php
__isset($name) #Vérifie si la variable en paramètere variable existe, si oui et a une valeur différente de NULL, renvoie TRUE sinon renvoie FALSE. Elle est appelée lorsque on essaye d'utiliser la fonction isset sur un objet ou un attribut qui n'existe pas
__unset($name) #__unset Détruit la (ou les) variable(s) en paramètre si elle existe. elle prend le nom de l'objet qu'on essaye de détuire mais auquel on a pas accès avec unset
__set($name, $value) #__set est implicitement appelée lorsque on essaye d'assigner une valeur a un objet auquel on a pas accès ou qui n'existe pas.La méthode prend deux paramètre le nom de l'objet ainsi que la valeur qu'on veut lui attribuer. aucun retour de la fonction
__get($name)#__get est appelé lorsque on cherche à accéder à un objet qui n'existe pas  / ou auquel on a pas accès. elle prend un paramètre qui est le nom de l'objet auquel on a n'a pas accès / qui n'existe pas. Elle peut renvoyer n'importe quelle valeur.
__construct()#__construct est la méthode magique appelée au moment de la création d'un objet, elle ne prend pas de paramètre
__destruct()#__destruct, Elle fonctionne de la même manièree que construct et est appelée à la destruction de l'objet, elle sera donc appelée implictement à la fin d'un script aussi
```

Question  3. 
C'est la méthode magique __destruct()


Question 4.

Classe abstraite

on peut les créer de la manière suivante: 
```php
abstract class ClassName {
}
```

Question 5.

```php
public # peut être utilisé à peu prêt n'importe où dans le code
private #se restreint seulement à la classe qui définie l'attribut
protected # se restraint à la classe qui définie l'attribue ainsi que toutes les classes qui en hérite.
```

Question 6. 

les exceptions sont les méthodes de gestion des erreurs. Elle utilise une classe nommée Exception, et se base sur le php orienté objet.

```php
throw #Lancement de l'exception en cas de détection de l'erreur
try #on va essayer d'exécuter certaines oppérations dans le bloc try
catch # on va rattraper les exceptions du try vis à vis de la donnée en paramètre du catch qui va lui dire quel type d'exception récuperer (sinon il prend toutes les exceptions
```

 Question 7. 

 Le routeur sert à rediriger entre les multiples pages liées d'un site de manière plus optimisée car cette méthode permet de réutiliser du code commun entre deux page sans devoir y rechager, c'est donc une optimisation. il utilise la variable super globale ` $_GET`

 Question 8.

 Les avantages sont:
 la factorisation du code (réutiliser du code existant plutôt que le réécrire)
 la propreté du code (via l'isolation des différents composant)
 la facilité de maintenance

 Question 9. 

 Il y a trois élément qui composent le pattern MVC

 Le modèle: Les classes définissant les objets de la BDD ainsi que les classes d'accès à cette dernière
 la vue: C'est ce que voit l'utilisateur lors de sa navigation, il affiche les données du modèle sans les modifier
 le contrôleur: c'est ce qui dicte ce que voit l'utilisateur pendant sa navigation, c'est le lien entre la vue et le modèle