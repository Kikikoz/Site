---
title: Plan
title-origin: Blueprints
traduction: stt
created_on: 20170707
modified_on: 
taxonomy:
    category: docs
---

1. [Qu'est ce qu'un Plan?](#what-is-a-blueprint)
1. [Type de Plan](#types-of-blueprints)
1. [Composants d'un Plan](#components-of-a-blueprint)

## Qu'est ce qu'un Plan?

Les plans sont une facette majeure de Grav. Ils sont les fondementaux d'un thèmes ou des intéractions entre un plugin avec le module d'administration de Grav. Ils déterminent ce que c'et un thème ou un plugin, son nom, où il est localisé sur GitHub, etc. Il produit également les options de configuration de ce thème ou de ce thème pour le module d'administration de Grav. 

Un plan est défini dans un fichier YAML, et peut la plupart du temps contenir des prorprités pour son hôte ainsi que des définitions pour les formulaires.

La grande majorité des utilisateur de Grav n'auront jamais a travailler avec ses Plan. Dit simplement, ils détérminent comment les plugins et les thèmes apparaissent dans le "backoffice" du site. Pour la plupart des utilisateurs,  c'est l'endroit où ils vont configurer les thèmes et les plugins en utilisant le module d'administration de Grav, ou manipuler les options à l'intérieur du thème ou du fichier principal (au format YAML) du plugin.

Les gens qui travailleront le plus avec ces Plans sont les developpeurs qui vont créer leur propres thèmes et plugins ou qui voudront personnaliser les options d'une ressource dans le "backoffice". Ce sont des outils très puissants qui définissent une ressource, où Grav va pouvoir trouver les mise à jour de cette ressource, et quelles sont les options de configuration qui sont susceptibles d'apparaitre dans le "backoffice".
