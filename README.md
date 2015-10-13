# DemoSliderCirculaire
Slider sous forme de cadran (genre compteur de vitesse) avec le zéro à 180°. Couleurs, rayon et valeurs paramétrables (int).

Pour utiliser ce composant, on doit préciser le rayon extérieur (en XAML ou en C#), puis :
- La liste des couleurs (en C#)
- La liste des valeurs (en C# aussi). Ici, j'ai mis 1,2,3,4,5,6 mais ça peut aussi bien être 1,10,100,1000,10000 ou autre chose.
Ces deux listes doivent avoir la même taille (Sinon, les premières valeurs de la plus grosse sont éliminées).
Le composant s'affiche dès que les deux listes ont été renseignées.

-----------------------------------------------------------------------------------------------------------------------------

Circlr slider

- Put a "Cadran" element in your XAML or add it in the code behind : 

    Cadran c = new Cadran();
    myGrid.Children.Add(c);
- Define the radius:
  - in xaml : \<myLibrary:Cadran Rayon="100"/>
  - or in the code behind : c.Rayon = 100;  
- Define the lists in the code behind:
  - list of values (int) : c.AddValeurs(12,42,7000);
  - list of colors : c.AddCouleurs(new SolidColorBrush(Colors.Red), new SolidColorBrush(Colors.Orange), new SolidColorBrush(Colors.Yellow));
