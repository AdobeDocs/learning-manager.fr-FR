---
description: Découvrez les API non connectées pour développer l’interface sans en-tête.
jcr-language: en_us
title: API non connectées
source-git-commit: 21e2a4a5e73fcbddb64e0afec0a896b315e38688
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# API non connectées

Pour en savoir plus sur les API Adobe Learning Manager, qui fournissent des données pour l’expérience sans tête ou hors connexion, consultez cet article.
API de recherche publique

## API de recherche publique

### Filtrage des données à l’aide de Public ES

L&#39;API de recherche publique vous permet d&#39;obtenir les données de filtre qui peuvent être utilisées avec l&#39;API de recherche de base pour filtrer les cours. Cette API fournit tous les filtres pouvant être utilisés dans l’API de recherche.

**Exemple de boucle**

Utilisez la méthode de GET pour effectuer la requête suivante. Remplacez &lt;Base_URL> par votre URL de base dans la commande de boucle ci-dessous. Vous trouverez l’&lt;Base_URL> sur la page du connecteur d’accès aux données de formation.

```
curl --location '<Base_URL>/filterableData'
```

**Exemple de réponse**

```
{
    "terms": {
        "loSkillLevels": [
            "1"
        ],
        "catalogNames": [
            "Default Catalog"
        ],
"catalogLabelIds": [
            "0000_1111"
        ],
        "loType": [
            "course"
        ],
        "availability": [
            "waitlistAvailable",
            "seatAvailable"
        ],
        "loSkillNames": [
            "General"
        ],
        "tags": [
            "course_tag"
        ],
        "authors": [
            "author_1"        
]
    },
    "range": {
        "duration": [
            "0"
        ],
        "dateCreated": [
            "2024-06-13T04:32:17.000Z"
        ],
        "price": [
            "0.0"
        ],
        "sessionEndTime": [
            "2024-06-18T20:30:00.000Z"
        ],
        "averageRating": [
            "0.0"
        ],
        "sessionStartTime": [
            "2024-06-18T19:30:00.000Z"
        ],
        "publishDate": [
            "2024-06-13T04:32:51.000Z"
        ],
        "ratingsCount": [
            "0"
        ]
    },
    "term": {}
}
```

**Options de filtre**

| Options | Description |
| --- | --- |
| `loSkillLevels` | Niveau de maîtrise requis pour s&#39;inscrire au cours. |
| `catalogNames` | Liste des noms de catalogue disponibles. |
| `loType` | Types d’objets d’apprentissage disponibles. |
| `availability` | Disponibilité des places et des listes d’attente. |
| `loSkillNames` | Noms de compétences ajoutés aux objets d’apprentissage. |
| `tags` | Balises associées aux objets d’apprentissage. |
| `authors` | Nom de l’auteur des objets d’apprentissage |
| `duration` | Durée des objets d’apprentissage. |
| `dateCreated` | Date de création de l’objet d’apprentissage. |
| `sessionEndTime` | Heure de fin de la session. |
| `averageRating` | Nombre moyen d’étoiles des objets d’apprentissage. |
| `sessionStartTime` | Heure de début de la session. |
| `publishDate` | Date de publication de l’objet d’apprentissage. |
| `ratingsCount` | Nombre d&#39;évaluations pour l&#39;objet d&#39;apprentissage. |

### API de recherche

L’API de recherche publique vous permet d’obtenir des données de recherche de base à l’aide des données fournies.

**Exemple de boucle**

Utilisez la méthode du POST pour effectuer la requête ci-dessous. Remplacez &lt;Base_URL> par votre URL de base dans la commande de boucle ci-dessous. Vous trouverez l’&lt;Base_URL> sur la page du connecteur d’accès aux données de formation.

```
curl --location '<Base_URL>/search?size=1000' \
--header 'content-type: application/json' 

--data '{
   "query": "",
   
    "sort": {
        "name": "publishDate",
        "order": "desc"
    },
    "lang": [
        "en-US"
    ],
    "filters": {
        "terms": {
            "loType": [
                "course",
                "learningProgram",
                "certification"
            ],
            "availability": [
                "seatAvailable",
                "waitlistAvailable"
            ]
        },
        "term": {
            "enrollmentDeadlinePassed": "true"
        },
        "range": {
                "dateCreated": [
                    {
                        "gte": "2024-05-02T02:48:51.000Z"
                    }
                ],
            "sessionStartTime": [
                {
                   "gte": "2024-06-18T19:30:00.000Z"
                }
            ],
            "sessionEndTime": [
                {
                   "lte": "2024-06-20T09:30:00.000Z"     
                }
            ]
        }
    }
}'
```

**Exemple de réponse de l&#39;appel API**

```
{
    "results": [
        {
            "loId": "course:11332313",
            "loType": "course",
            "tags": [
                "course_tag"
            ],
            "authors": [
                "author1",
                "author2"
            ],
            "status": "Published",
            "duration": 0,
            "publishDate": "2024-06-13T04:32:51.000Z",
            "dateCreated": "2024-06-13T04:32:17.000Z",
            "name": "vc coursse to check ",
            "averageRating": 0.0,
            "ratingsCount": 0,
            "loSkillNames": [
                "General"
            ],
            "loSkillLevels": [
                "1"
            ],
            "loInstances": [
                {
                    "id": "14346696",
                    "name": "Default Instance",
                    "status": "Active",
                    "price": 0.0
                }
            ],
            "catalogInfo": [
                {
                    "id": "37779",
                    "name": "Default Catalog"
                }
            ]
        }
    ],
    "request": {
        "query": "",
        "filters": {
            "terms": {
                "loType": [
                    "course",
                    "learningProgram",
                    "certification"
                ],
                "loSkillNames": [
                    "General"
                ],
                "deliveryType": [],
                "availability": [
                    "seatAvailable",
                    "waitlistAvailable"
                ]
            },
            "term": {
                "enrollmentDeadlinePassed": "true"
            },
            "range": {
                "dateCreated": [
                    {
                        "gte": "2024-05-02T02:48:51.000Z"
                    }
                ],
                "sessionStartTime": [
                    {
                        "gte": "2024-06-18T19:30:00.000Z"
                    }
                ],
                "sessionEndTime": [
                    {
                        "lte": "2024-06-20T09:30:00.000Z"
                    }
                ]
            }
        },
        "sort": {
            "name": "publishDate",
            "order": "desc"
        },
        "lang": [
            "en-US"
        ]
    },
    "self": "<Base_URL>/search?page=0&size=1000",
    "count": 1
}
```

**Options de tri sur l&#39;API de recherche**

Vous pouvez sélectionner les options de tri suivantes à appliquer aux résultats.

| Options | Description |
| --- | --- |
| `duration` | Durée de l’objet d’apprentissage. |
| `publishDate` | Date de publication de l’objet d’apprentissage. |
| `dateCreated` | Date de création de l’objet d’apprentissage. |
| `name_en` | Nom de l’objet d’apprentissage. |
| `averageRating` | Évaluation moyenne par étoiles fournie par les élèves. |
| `ratingsCount` | Nombre d&#39;évaluations pour l&#39;objet d&#39;apprentissage. |
| `relevance(default)` | Les données pertinentes sont basées sur les mots-clés de recherche. |

### Obtention des données des objets d’apprentissage à l’aide de l’API de recherche publique

L’API d’objet d’apprentissage ES public vous permet d’obtenir la liste des types et des ID des objets d’apprentissage disponibles sur l’interface sans en-tête.

**Exemple de boucle**

Utilisez la méthode de GET pour effectuer la requête suivante. Remplacez &lt;Base_URL> par votre URL de base dans la commande de boucle ci-dessous. Vous trouverez l’&lt;Base_URL> sur la page du connecteur d’accès aux données de formation.

```
curl --location '<Base_URL>/learningObjectIds'
```

**Exemple de réponse pour l&#39;appel API**

```
{
    "loIds": [
        "course:1132800",
"certification:126009",
"learningProgram:104433"
    ]
}
```

## API de résumé de cours

L&#39;API de résumé de cours vous permet de récupérer des informations détaillées sur un cours spécifique.

**Exemple de boucle**

Utilisez la méthode de GET pour effectuer la requête suivante. Remplacez &lt;Base_URL> par votre URL de base dans la commande de boucle ci-dessous. Vous trouverez l’&lt;Base_URL> sur la page du connecteur d’accès aux données de formation. Remplacez &lt;Course_ID> par l’ID de cours spécifique.

```
curl --location '<Base_URL>/loSummary?loId=course%3A<Course_ID>'
```

**Exemple de réponse de l&#39;appel API**

```
{
    "results": [
        {
            "instanceId": "14336686",
            "courseId": "11312313",
            "accountId": "44355",
            "seatConsumed": 1,
            "seatLimit": 1,
            "waitlistLimit":1,
            "waitlistCount": 1,
            "seatAvailable": false,
            "waitlistAvailable": false
        }
    ],
    "count": 1
}
```

>[!NOTE]
>
>Si un cours comporte plusieurs instances, vous obtiendrez des détails pour toutes les instances.

## API CDN JSON pour les détails du cours

L&#39;API CDN JSON vous permet de récupérer les informations complètes sur un cours spécifique.

**Exemple de boucle pour le cours**

Utilisez la méthode de GET pour effectuer la requête suivante. Remplacez &lt;chemin_CDN> par votre URL de base dans la commande de boucle ci-dessous. Vous trouverez le &lt;chemin_CDN> sur la page du connecteur d’accès aux données de formation. Remplacez &lt;Course_ID> par l’ID de cours spécifique.

```
curl --location '<CDN_path_URL>/course/<Course_ID>.json'
```

**Exemple de boucle pour le parcours d’apprentissage et la certification**

```
curl --location '<CDN_path_URL>/learningProgram/<LearningProgram_ID>.json'
```

```
curl --location '<CDN_path_URL>/ certification /<Certification_ID>.json'
```

**Exemple de réponse de l&#39;appel API**

```
{
    "data": {
        "id": "course:11342313",
        "type": "learningObject",
        "attributes": {
            "authorNames": [
                "author1",
                "author2"
            ],
            "dateCreated": "2024-06-13T04:32:17.000Z",
            "datePublished": "2024-06-13T04:32:51.000Z",
            "dateUpdated": "2024-06-13T04:32:51.000Z",
            "duration": 0,
            "effectiveModifiedDate": "2024-06-13T04:32:51.000Z",
            "effectivenessIndex": 0,
            "enrollmentType": "Self Enroll",
            "hasOptionalLoResources": false,
            "hasPreview": false,
            "isExternal": false,
            "isMqaEnabled": false,
            "isPrerequisiteEnforced": false,
            "isSubLoOrderEnforced": false,
            "loResourceCompletionCount": 1,
            "loType": "course",
            "moduleResetEnabled": false,
            "state": "Published",
            "tags": [
                "course_tag"
            ],
            "unenrollmentAllowed": true,
            "localizedMetadata": [
                {
                    "description": "",
                    "locale": "en-US",
                    "name": "vc coursse to check "
                }
            ],
            "rating": {
                "averageRating": 0,
                "ratingsCount": 0
            }
        },
        "relationships": {
            "authors": {
                "data": [
                    {
                        "id": "13138897",
                        "type": "user"
                    }
                ]
            },
            "instances": {
                "data": [
                    {
                        "id": "course:11332313_14336696",
                        "type": "learningObjectInstance"
                    }
                ]
            },
            "skills": {
                "data": [
                    {
                        "id": "course:11332313_237719",
                        "type": "learningObjectSkill"
                    }
                ]
            }
        }
    },
    "included": [
        {
            "id": "237719",
            "type": "skill",
            "attributes": {
                "name": "General",
                "state": "Active"
            },
            "relationships": {
                "levels": {
                    "data": [
                        {
                            "id": "237719_1",
                            "type": "skillLevel"
                        }
                    ]
                }
            }
        },
        {
            "id": "course:11312313",
            "type": "learningObject",
            "attributes": {
                "authorNames": [
                    "m 41",
                    "rae"
                ],
                "dateCreated": "2024-06-13T04:32:17.000Z",
                "datePublished": "2024-06-13T04:32:51.000Z",
                "dateUpdated": "2024-06-13T04:32:51.000Z",
                "duration": 0,
                "effectiveModifiedDate": "2024-06-13T04:32:51.000Z",
                "effectivenessIndex": 0,
                "enrollmentType": "Self Enroll",
                "hasOptionalLoResources": false,
                "hasPreview": false,
                "isExternal": false,
                "isMqaEnabled": false,
                "isPrerequisiteEnforced": false,
                "isSubLoOrderEnforced": false,
                "loResourceCompletionCount": 1,
                "loType": "course",
                "moduleResetEnabled": false,
                "state": "Published",
                "tags": [
                    "course_tag"
                ],
                "unenrollmentAllowed": true,
                "localizedMetadata": [
                    {
                        "description": "",
                        "locale": "en-US",
                        "name": "course name "
                    }
                ],
                "rating": {
                    "averageRating": 0,
                    "ratingsCount": 0
                }
            },
            "relationships": {
                "authors": {
                    "data": [
                        {
                            "id": "13128897",
                            "type": "user"
                        }
                    ]
                },
                "instances": {
                    "data": [
                        {
                            "id": "course:11312313_14336696",
                            "type": "learningObjectInstance"
                        }
                    ]
                },
                "skills": {
                    "data": [
                        {
                            "id": "course:11312313_237719",
                            "type": "learningObjectSkill"
                        }
                    ]
                }
            }
        },
        {
            "id": "course:11312313_14336696_12034506_0",
            "type": "learningObjectResource",
            "attributes": {
                "externalReporting": false,
                "isExpiredSubmission": false,
                "loResourceType": "Content",
                "multipleAttemptEnabled": false,
                "previewEnabled": false,
                "resourceType": "Virtual Classroom",
                "submissionEnabled": false,
                "localizedMetadata": [
                    {
                        "description": "",
                        "locale": "en-US",
                        "name": "vc session"
                    }
                ]
            },
            "relationships": {
                "learningObject": {
                    "data": {
                        "id": "course:11312313",
                        "type": "learningObject"
                    }
                },
                "resources": {
                    "data": [
                        {
                            "id": "course:11312313_14336696_12034506_0_resource",
                            "type": "resource"
                        }
                    ]
                }
            }
        },
        {
            "id": "course:11312313_237719",
            "type": "learningObjectSkill",
            "attributes": {
                "credits": 1,
                "learningObjectId": "course:11312313"
            },
            "relationships": {
                "skillLevel": {
                    "data": {
                        "id": "237719_1",
                        "type": "skillLevel"
                    }
                }
            }
        },
        {
            "id": "13128897",
            "type": "user",
            "attributes": {
                "avatarUrl": "https://abccontents.adobe.com/public/images/default_user_avatar.svg",
                "binUserId": "1f8c01aa-7f58-42e9-bc40-11537eb6498d",
                "email": "manjusha+41re@adobetest.com",
                "enrollOnClick": false,
                "gamificationEnabled": true,
                "lastLoginDate": "2024-06-13T04:23:45.000Z",
                "name": "m 41",
                "pointsEarned": 0,
                "pointsRedeemed": 0,
                "preferredResolution": "AUTO",
                "profile": "admin",
                "roles": [
                    "Learner",
                    "Admin",
                    "Author",
                    "Instructor",
                    "Integration Admin"
                ],
                "state": "ACTIVE",
                "userType": "Internal"
            },
            "relationships": {
                "account": {
                    "data": {
                        "id": "44355",
                        "type": "account"
                    }
                }
            }
        },
        {
            "id": "course:11312313_14336696_12034506_0_resource",
            "type": "resource",
            "attributes": {
                "avatarUrls": [
                    "https://abccontents.adobe.com/public/images/default_user_avatar.svg"
                ],
                "completionDeadline": "2024-06-18T20:30:00.000Z",
                "contentType": "Virtual Classroom",
                "dateStart": "2024-06-18T19:30:00.000Z",
                "desiredDuration": 3600,
                "hasQuiz": false,
                "hasToc": false,
                "instructorNames": [
                    "instructor1"
                ],
                "isDefault": true,
                "locale": "en-US",
                "location": "http://google.com",
                "name": "vc session",
                "onlyQuiz": false,
                "reportingType": "NONE"
            }
        },
        {
            "id": "course:11312313_14336696",
            "type": "learningObjectInstance",
            "attributes": {
                "dateCreated": "2024-06-13T04:32:18.000Z",
                "isDefault": true,
                "isFlexible": false,
                "state": "Active",
                "localizedMetadata": [
                    {
                        "locale": "en-US",
                        "name": "Default Instance"
                    }
                ],
                "seatConsumed": 0,
                "waitlistCount": 0
            },
            "relationships": {
                "learningObject": {
                    "data": {
                        "id": "course:11312313",
                        "type": "learningObject"
                    }
                },
                "loResources": {
                    "data": [
                        {
                            "id": "course:11312313_14336696_12034506_0",
                            "type": "learningObjectResource"
                        }
                    ]
                }
            }
        },
        {
            "id": "237719_1",
            "type": "skillLevel",
            "attributes": {
                "level": "1",
                "maxCredits": 1,
                "name": "Level 1"
            },
            "relationships": {
                "skill": {
                    "data": {
                        "id": "237719",
                        "type": "skill"
                    }
                }
            }
        }
    ]
}
```
