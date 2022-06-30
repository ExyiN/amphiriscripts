# Amphiris Skript

## Objets cliquables

### Comment créer un objet cliquable

Dans le fichier `cliquable-objects.sk`, ajoutez ces lignes là dans l'événement souhaité.  
Les événements possibles :  
```
on right click: // clic droit

on left click: // clic gauche
```
#### Clic d'un objet dans la main principale :
```
if name of player's tool is "nom":
    cancel event
    make player execute command "commande" // Joueur qui exécute
    make console execute command "commande" // Console qui exécute
    stop
```

#### Clic d'un objet dans la main secondaire :
```
if name of offhand tool is "nom":
    cancel event
    make player execute command "commande" // Joueur qui exécute
    make console execute command "commande" // Console qui exécute
    stop
```

Le `cancel event` permet d'annuler l'évément produit par le clic.  
Ex : Annule l'ouverture du four si on regardait le four.

#### Structure du fichier :

Quand vous ajoutez un objet, mettez un commentaire pour savoir ce que fait l'objet.  
Pour mettre un commentaire dans un fichier, il faut utiliser le caractère `#`.

**Exemple de structure :**
```
on right click:
    # Objet qui fait coucou à Robert
    if name of player's tool is "Robert":
        cancel event
        make player execute command "/msg Robert COUCOU ROBERT"
        stop

    # Objet qui kick Jason
    if name of offhand tool is "Jason":
        cancel event
        make console execute command "/kick Jason"
        stop
    
    // etc.
```
