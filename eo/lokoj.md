
# Fontoj por lokoj
* http://gov.genealogy.net/
* http://geo.api.gouv.fr/ kaj https://api.insee.fr/
* https://www.geonames.org/v3/

# specoj de lokoj

| gramps kodo | gramps eo     | gramps fr                 | gov | gouv.fr        | geonames.org |
|-------------|---------------|---------------------------|-----|----------------|--------------|
| 1           | Lando         | Pays                      |     | Pays           |  PCLI        |
| 2           | Ŝtato         | Province (Région)         |     |                |              |
| 3           | Provinco      | Comté (Départ.)           |     |                |              |
| 4           | Urbo          | Ville                     |     |                |              |
| 5           | Paroko        | Paroisse                  |     |                |              |
| 6           | Loko          | Lieu-dit                  |     |                |              |
| 7           | Strato        | Rue                       |     |                |              |
| 8           | Provinco      | Province                  |     |                |              |
| 9           | Regiono       | Région                    |     | Région         | ADM1         |
| 10          | Departmento   | Département               |     | Département    | ADM2         |
| 11          | Proksimeco    | Quartier                  |     |                |              |
| 12          | Distrikto     | District (Arrondissement) |     |                |              |
| 13          | Urbodistrikto |	Borough (Arrondissement)  |     | Arrondissement | ADM3         |
| 14          | Municipo      | Municipalité              |     | Commune        | ADM4         |
| 15          | Urbo          | Bourg                     |     |                |              |
| 16          | Vilaĝo        | Village                   |     |                |              |
| 17          | Vilaĝeto      | Hameau                    |     |                |              |
| 18          | Farmo         | Ferme                     |     |                |              |
| 19          | Konstruaĵo    | Immeuble                  |     |                |              |
| 20          | Numero        | Numéro                    |     |                |              |


# aldonaĵoj

* getgov
  * interfaco kun http://gov.genealogy.net/
* PlaceFrCog
  * interfaco kun http://api.gouv.fr/  
* PlaceCleanupGramplet
  * interfaco kun http://www.geonames.org/
* PlaceUpdate
* PlaceCoordinatesGramplet
* PlaceCoordinateGeoView
* PlaceCompletion
* ExtractCity
* GoogleEarthWriteKML
