# GroceryApp sprint3 Studentversie  
    
## UC07 Delen boodschappenlijst  
Is compleet  
  
## UC08 Zoeken producten  
Aanvullen:
- In de GroceryListItemsView zitten twee Collection Views, namelijk één voor de inhoud van de boodschappenlijst en één voor producten die je toe kunt voegen aan de boodschappenlijst  
- Voeg boven de tweede CollectionView een zoekveld (SearchBar) in om op producten te kunnen zoeken.  
- Zorg dat de SearchCommand wordt gebonden aan een functie in het onderliggende ViewModel (GroceryListItemsViewModel) en dat de zoekterm die in het zoekveld is ingetypt gebruikt wordt als parameter (SearchCommandParameter).  
- Werk in het viewModel (GroceryListItemsViewModel) de zoekfunctie uit en zorg dat de beschikbare producten worden gefilterd op de zoekterm!  

## UCx Registratie gebruiker 
Of een ander idee zelf uitwerken. Dit betekent ook dat de documentatie hiervoor ontwikkeld moet worden.

## GitFlow beschrijving
Ik maak gebruik van een eenvoudige branchin-strategie gebaseerd op GitFlow-principes.
De kernregels van deze branching strategie gaan als volgt.

* Main: de mainbranch bevat alleen geteste, productieklaar code. Merges van dev gebeuren hier na volledige validatie.
* dev: Integratiebranch voor het samenvoegen van alle features/ bugfixes. Hier draaien de pipelines vor tests en builds.

# Feature branches:
* Naamconventie gaat als volgt: feature/<FEATURECODE> (bijv. feature/UC1).
* Doel: Nieuwe functionaliteiten ontwikkelen.
* Workflow: Nieuwe branch gebasseerd op dev, na het implementeren van de functionaliteit merge naar dev via een pull request.

# Bugfix branches:
* Naamconventie gaat als volgt: bugfix/<BUGBESCHRIJVING> (bijv. bugfix/YML1)
* Doel: oplossen van bugs
* Workflow: Nieuwe branch gebasseerd op dev, na het oplossen van de bug merge naar dev via een pull request.

# Workflow
1. Maak een nieuwe branch gebasseerd op dev (bijv. git checkout -b feature/UC1 dev)
2. Ontwikkel en commit
* Gebruik conventionele commit berichten
* Push regelmatig
3. Merge naar dev
* Maak een pullrequest van je feature/bug branch naar dev
* Review (door jezelf tijdens deze sprints)
4. Integratie en testen
* Na het mergen naar dev, triggeren de pipelines automatisch
* Kijk op het einde zelf nog goed door de code heen voordat er een merge request naar main gaat
5. Release naar main
* Wanneer dev goed is en de pipelines zijn geslaagt, merge dev naar main via een pullrequest
* Tag de release (bijv. v0.0.1  commando: git tag v0.0.1)

# Extra informatie
* Geen directe pushes naar main of dev, altijd via pull requests werken.
* Verwijder een feature of bugfix branch na een pull request
