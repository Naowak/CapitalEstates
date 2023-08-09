# CapitalEstates
Capital Estates: The Bernard Arnault Edition


https://ville-data.com/logement/Bordeaux-33-33063

https://www.alliance-habitat.com/investissement-locatif/logement-decent/taille-logement/

https://cadastre.data.gouv.fr/data/dgfip-pci-vecteur/2023-07-01/edigeo/departements/

https://www.meilleursagents.com/prix-immobilier/eysines-33320/

https://www.insee.fr/fr/metadonnees/cog/arrondissement/ARR332-bordeaux


On prends toutes les villes d'une zone géographique selon l'insee (pour cet exemple, bordeaux)

On récupère sur ville-data.com les stats sur cette ville concernant le nombre de logement, la répartition (maison - appartmement) et la compositions.

Seulement, la répartition des logements (t1, t2, t3, t4, t5, t6) est compté seulement pour les logements principaux.

On va donc prendre la répartition des logements principaux et l'appliquer aux logements totaux.

Ensuite, on s'intéresse au DVF pour réussir à estimer la taille moyenne des logements en fonction du nombre de pièces.

Pour simplifier l'opération, on réuni tous les logements ayant plus de 5 pièces en un seul groupe : 5+.

On calcul ensuite la moyenne de la taille des logements en fonction du nombre de pièces, du type de logement (appart, maison) et de leur ville.

On récupère ensuite le prix moyen au m2 pour chaque ville sur meilleursagents.com