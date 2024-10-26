# IWADI_Project

## API de Recommandation de Parcours Étudiants

### Présentation

Cette API RESTful a pour objectif de fournir des recommandations de parcours d'études personnalisées aux étudiants, en fonction de leurs critères de recherche (niveau d'étude, spécialité, matières préférées, métier, passion). Les résultats sont catégorisés (Excellent, Ecole publique, Ecole privée, Classique) et sont alimentés par une IA avancée.

### Fonctionnalités

  * __Recommandations personnalisées__ : L'API retourne des parcours d'études adaptés au profil de chaque étudiant.
  * __Catégorisation des résultats__ : Les parcours sont classés en différentes catégories pour faciliter la prise de décision.
  * __Intégration avec un agent IA__ : L'API s'appuie sur une IA sophistiquée pour effectuer des recherches approfondies et fournir des résultats pertinents.


### Points d'entrée (Endpoints)

#### GET /parcours

* __Paramètres__ :
  * __niveau__ : Niveau d'étude (bac, licence, master, etc.)
  * __specialite__ : Spécialité souhaitée
  * __matieres__ : Liste de matières préférées (séparées par des virgules)
  * __metier__ : Métier visé
  * __passion__ : Passion ou intérêt particulier

* __Réponse__ : Un tableau de parcours, chaque parcours étant un objet JSON avec les propriétés suivantes :

  * __category__ : Catégorie du parcours (Excellent, Ecole publique, etc.)
  * __formations__ : Tableau de formations, chaque formation étant un objet JSON avec les propriétés suivantes :
  * __niveau__ : Niveau d'étude
  * __filiere__ : Filière
  * __ecoles__ : Liste d'écoles
  * __domaine__ : Domaine d'étude
  * __description__ : Description détaillée du parcours
 
### Exemple de réponse :

```json
[
  {
    "category": "Excellence",
    "formations": [
      {
        "niveau": "Licence",
        "filiere": "Licence statistique",
        "ecoles": [
          "African School of Economics",
          "Ecole Nationale d'Economie"
        ],
        "domaine": "Statistiques & Economie",
        "description": null
      }
    ]
  },
  {
    "category": "Ecole privée",
    "formations": [
      {
        "niveau": "Licence",
        "filiere": "Licence statistique",
        "ecoles": [
          "African School of Economics",
          "Ecole Nationale d'Economie"
        ],
        "domaine": "Statistiques & Economie",
        "description": null
      }
    ]
  }
]
