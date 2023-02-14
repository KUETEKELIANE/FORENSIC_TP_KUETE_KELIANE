# H1 EXERCICE

Dans le fishier CSV, faire le tri des enregistrements de la consommation-annuelle-residentielle-par-adress donc le type-de-voie de la colone "F" est AVENUE par ordre alphabetique.

## H2 SOLUTION

Pour trier les enregistrées de la consommation-annuelle-résidentielle-par-adresse dont le type-de-voie de la colonne "F" est "AVENUE", il faut utiliser:
1. First item la commande "grep" pour filtrer les enregistrés correspondants,
2. Second item puis utiliser la commande "sort" pour trier ces enregistrements par ordre alphabétique.

La commende est dont la suivante:
grep ',AVENUE,' consommation-annuelle-residentielle-par-adresse.csv | sort -t ',' -k 1

Dans cette commande, la première partie "grep ',AVENUE,' consommation-annuelle-residentielle-par-adresse.csv" filtre les enregistrés pour n'inclure que ceux qui ont "AVENUE" comme type-de-voie. La virgule avant et après "AVENUE" sert à s'assurer que nous ne sélectionnons que les enregistrements où "AVENUE" est une valeur complète dans la colonne, plutôt qu'une partie d'une autre valeur (par exemple, "AVENUE De ....").

Ensuite, la seconde partie "| sort -t ',' -k 1" trie les extraits filtrés par ordre alphabétique de la première colonne. Si vous voulez trier par une autre colonne, remplacez "1" par le numéro de la colonne que vous voulez trier.
