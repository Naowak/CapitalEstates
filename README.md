# Capital Estates : The Bernard Arnault Edition

### Description

Ce projet vise à quantifier la quantité de logement que Bernard Arnault pourrait acheter avec sa fortune estimée 212,7 milliards d'euros [(selon Forbes, juil. 2023)](https://www.forbes.fr/classements/classement-milliardaires-forbes-2023-2-bernard-arnault-lempereur-du-luxe-au-210-milliards-de-fortune/).  

Je m'intéresse à la ville de Bordeaux et ses alentours, ainsi qu'a la ville de Paris. Il s'agit donc en premier lieu d'estimée la valeur de tous les logements d'une ville à partir de données publiques. Puis, de calculer le nombre de logements que l'on peut acheter avec la fortune de Bernard Arnault.

![Paris](/infographie-paris.png)
![Bordeaux](/infographie-bordeaux.png)

### Méthodologie d'Estimation de la Valeur des Logements par Ville

1. **Sélection de la Ville** : 
   - On choisit toutes les villes d'une région donnée, comme défini par l'INSEE. Pour cette démonstration, nous prendrons l'exemple de Bordeaux.

2. **Collecte des Données des Logements** :
   - On se rend sur ville-data.com pour obtenir les statistiques de chaque ville. Ces statistiques nous renseignent sur la quantité de chaque type de logement (maison ou appartement).
   - On y trouve aussi une répartition des logements selon leur nombre de pièces : t1, t2, t3, t4, t5+.
   
3. **Correction des Données** :
   - Attention, la répartition par nombre de pièces est disponible uniquement pour les logements principaux. Pour avoir une vue d'ensemble, on extrapolera ces statistiques aux logements totaux en utilisant le même ratio.

4. **Estimation de la Taille des Logements** :
   - On utilise la base de données DVF pour estimer pour chaque ville la taille moyenne d'un logement en fonction du nombre de pièces.
   - Si une ville a moins de 5 ventes enregistrées pour un certain nombre de pièces et type de logement, nous utilisons la taille moyenne fournie par alliance-habitat pour ce nombre de pièce et type de logement.

5. **Estimation de la Valeur des Logements** :
   - On consulte meilleursagents.com pour connaître le prix au mètre carré pour chaque ville et type de logement.
   - En multipliant ce prix au mètre carré par la taille moyenne des logements (selon le nombre de pièces et le type de logement), nous obtenons une estimation de la valeur totale des logements dans une ville donnée.

### Pré-requis (DVF)

Téléchager les fichiers suivants et les placer dans le dossier `data/` :

- dvf2018.txt 
- dvf2019.txt
- dvf2020.txt
- dvf2021.txt
- dvf2022.txt

Pour télécharger les DVF :
https://www.data.gouv.fr/fr/datasets/demandes-de-valeurs-foncieres/


### Installation

1. Cloner le projet

```
git clone git@github.com:Naowak/CapitalEstates.git
```

2. Installer les dépendances

```
pip install -r requirements.txt
```

3. Run the notebook

### Sources des données (Bordeaux)

Pour ce faire, nous allons utilise les données suivantes : 

- [Liste des villes de l'agglomération de Bordeaux selon l'INSEE](https://www.insee.fr/fr/metadonnees/cog/arrondissement/ARR332-bordeaux)

- [Prix au mètre carré par ville et type de logement selon meilleursagents.com](https://www.meilleursagents.com/prix-immobilier/bordeaux-33000/)

- [Nombre et répartition de logements par ville selon ville-data.com](https://ville-data.com/logement/Bordeaux-33-33063)

- [Taille moyenne des logements par ville selon alliance-habitat](https://www.alliance-habitat.com/investissement-locatif/logement-decent/taille-logement/)

- [Population par ville selon ville-data.com](https://ville-data.com/nombre-d-habitants/Bordeaux-33-33063)

- [Données cadastrales par ville selon cadastre.data.gouv.fr](https://cadastre.data.gouv.fr/data/etalab-cadastre/2023-07-01/geojson/departements/)


### Sources des données (Paris)

Pour ce faire, nous allons utilise les données suivantes :

- [Liste des arrondissements de Paris selon l'INSEE](https://www.insee.fr/fr/metadonnees/cog/departement/DEP75-paris)

- [Prix au mètre carré par arrondissement et type de logement selon meilleursagents.com](https://www.meilleursagents.com/prix-immobilier/paris-1er-arrondissement-75001/)

- [Nombre et répartition de logements par arrondissement selon ville-data.com](https://ville-data.com/logement/Paris-1er-Arrondissement-75-75101)

- [Taille moyenne des logements par arrondissement selon alliance-habitat](https://www.alliance-habitat.com/investissement-locatif/logement-decent/taille-logement/)

- [Population par arrondissement selon ville-data.com](https://www.insee.fr/fr/statistiques/fichier/6683031/dep75.pdf)

- [Données cadastrales par arrondissement selon cadastre.data.gouv.fr](https://cadastre.data.gouv.fr/data/etalab-cadastre/2023-07-01/geojson/departements/)