---
lang: fr
lang-niv: fonto
lang-ref: 001-debut
layout: page
kategorio: Présentation
title: Schémas simplifiés des données
mermaid: true
---

Avant de rentrer dans gramps, il est important de comprendre comment sont organisées les données.

# L'univers familial

Les trois objets essentiels qui vont vous permettre de construire votre arbre sont :
* l'individu :   
  la base de votre généalogie.
* la famille :  
  une famille dans gramps est constituée de un ou deux individus \(classiquement le mari et la femme, mais gramps autorise toutes les combinaisons\), et d'enfants. Elle va permettre de construire l'arbre.
* l'évènement :  
  un évènement est constitué principalement d'un type, d'une date \(ou une pèriode\), et d'une description.  
  Par exemple la naissance, la déclaration de naissance, le décès, le mariage, la profession vont être saisis dans un évènement.
  L'évènement peut être référencé par des individus et/ou des familles.

<div class="mermaid">
  erDiagram
    Famille ||--o| Individu : "Mari/conjoint"
    Famille ||--o| Individu : "Femme/conjoint"
    Famille ||--o{ Individu : "Enfants"
    Famille ||--o{ "Évènements" : participe
    Individu ||--o{ "Évènements" : participe
    Individu{
      Nom Nom_Principal
      liste_de_Nom Noms_Alternatifs
    }
    Famille{
      Texte Type
    }
    "Évènements"{
      Texte Type
      Date Date_de_l_evenement
      Texte Description
      Lieu  lieu_de_l_evenement
    }

</div>

# L'univers des sources
Sourcer votre généalogie est essentiel pour sa validation.  
Vous disposez de trois objets pour gérer les sources :
* la citation :  
  C'est l'élément le plus fin des sources, celui qui va être référencé par l'individu, la famille, l'évènement, le lieu, le média.  
  Par exemple ça va être l'acte de naissance trouvé dans un registre, un paragraphe dans un livre ou une revue…
  La citation est reliée à une source.
* la source :  
  La source est le support dans lequel vous puisez vos citations.  
  Ça peut être un registre, un microfilm, un livre…
  La source est localisée dans un ou plusieurs dépôts.
* les dépôts :  
  Le dépôt permet de regrouper les sources.  
  Ça peut être une archive départementale, un site internet, votre coffre-fort …  
  Une source peut se trouver dans plusieurs dépôts.  
  Malheureusement, la hiérarchie des sources s'arrête là. On aurait pu souhaiter qu'un dépôt fasse partie d'un autre dépôt, mais gramps ne le prend pas en charge actuellement.
<div class="mermaid">
  erDiagram
    Citation ||--o| Source : dans
    Source ||--o{ "Dépôt" : "conservée dans (type de support, cote)"
    Citation{
      Date date_de_l_evenement
      Volume_Page emplacement_dans_la_source
      niveau niveau_de_confiance
    }
    Source{
      Texte Titre
      Texte Auteurs
      Texte Infos_publication
      Texte Abbreviation
    }
    "Dépôt"{
      Texte Nom
      Texte Type
      Adresse   Adresse
      liste_de_liens Liens_internet
    }
</div>

# Les objets annexes
Enfin quatre objets pour enrichir vos données :
* le média :  
   Permet d'intégrer un fichier dans l'arbre. Ça peut être une image, une vidéo, un PDF, ou n'importe quoi d'autre.  
   On va pouvoir le relier à des individus, des familles, des évènements, des citations ou des lieux.
* la note :  
   Constituée d'un titre et d'un texte\(multiligne et formatable\).  
   Fort Utile ! Peut être reliée à n'importe quel objet ou référence d'objet.
   Permet de renseigner le contenu des documents, de saisir des pistes de recherche et bien d'autres choses.
   Une note peut être reliée à plusieurs objets.
* le lieu :  
  Pour ne pas ressaisir n fois la même chose, éviter les erreurs de recopie, localiser précisément les lieux où se sont produits vos évènements.  
  Les lieux peuvent s'emboîter les uns dans les autres \(exemple : pays --> département --> commune --> hameau\).  
  Avant de commencer à saisir les lieux, vous devriez bien réfléchir à votre manière d'organiser les lieux, et au greffon qui vous permettra de les gérer.
* l'étiquette
  Elles sont gérables par le menu «Édition»-->«Étiquette»   
  Sur chaque objet vous pouvez mettre des étiquettes.  
  Une étiquette est un texte court, auquel est associé une couleur.  
  Les étiquettes peuvent être utilisées :
  * pour filtrer
  * pour mettre en évidence dans les listes ou dans la vue graphique, grâce à la couleur.

# le schéma complet
Si vous souhaitez aller davantage dans le détail, le schéma de la base de données gramps peut être consulté ici : <https://gramps-project.org/wiki/index.php/Gramps_Data_Model>


# Premières saisies
## créer un individu
## ajouter un évènement à un individu
## ajouter les parents
## ajouter un conjoint
## ajouter un enfant
## ajouter une citation

# Aller plus loin
## les lieux
## les notes
## les étiquettes
## les médias


# Où obtenir de l'aide ?
* la documentation officielle : <https://gramps-project.org/wiki/index.php/Gramps_5.1_Wiki_Manual>
* le discourse de gramps : <https://gramps.discourse.group/> \(en anglais\)
* le forum geneanet : <https://www.geneanet.org/forum/viewforum.php?f=55945&sid=de725cd97855d4a68268a420061b629f> \(en français\)
