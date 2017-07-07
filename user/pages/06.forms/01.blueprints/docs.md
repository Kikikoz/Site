---
title: Desseins
title-origin: Blueprints
traduction: stt
created_on: 20170707
modified_on: 
taxonomy:
    category: docs
---

1. [Qu'est ce qu'un Dessein ?](#what-is-a-blueprint)
1. [Type de Dessein](#types-of-blueprints)
1. [Composants d'un Dessein](#components-of-a-blueprint)

## Qu'est ce qu'un Dessein ( NdT Blueprints en VO)?

Les desseins sont une facette majeure de Grav. Ils sont les fondementaux d'un thèmes ou des intéractions entre un plugin avec le module d'administration de Grav. Ils déterminent ce que c'et un thème ou un plugin, son nom, où il est localisé sur GitHub, etc. Il produit également les options de configuration de ce thème ou de ce thème pour le module d'administration de Grav. 

Un dessein est défini dans un fichier YAML, et peut la plupart du temps contenir des propriétés pour l'élément avec lequel il intéragit mais aussi des définitions pour les formulaires.

La grande majorité des utilisateur de Grav n'auront jamais a travailler avec ses Desseins. Dit simplement, ils déterminent comment les plugins et les thèmes apparaissent dans le "backoffice" du site. Pour la plupart des utilisateurs,  c'est l'endroit où ils vont configurer les thèmes et les plugins en utilisant le module d'administration de Grav, ou manipuler les options à l'intérieur du thème ou du fichier principal (au format YAML) du plugin.

Les gens qui travailleront le plus avec ces Desseins sont les développeurs qui vont créer leur propres thèmes et plugins ou qui voudront personnaliser les options d'une ressource dans le "backoffice". Ce sont des outils très puissants qui définissent une ressource, où Grav va pouvoir trouver les mise à jour de cette ressource, et quelles sont les options de configuration qui sont susceptibles d'apparaitre dans le "backoffice".

## Types de Dessein

Grav utilise le Dessein afin de:

- définir des informations sur les themes et plugins.
- définir les options de configuration des theme/plugin qui doivent être affiché en mode Administration.
- définir les  pages de formulaires dans le module d' Administration.
- définir les options affichées dans la partie Configuration de la section administration.

A présent, nous allons entrer dans les détails sur le fonctionnement des Desseins dans Grav.

#### Themes et Plugins

Quand ils sont utilsés dans les thèmes et plugins, la convention est de mettre un fichier **blueprints.yaml** (NdT:blueprints a été  traduit par dessein) dans le package. Se faisant, Grav peut connatre les metadonnées de cette  ressource, et de fait les introduire dans l'administration de Grav.


Ün fichier dessein (**blueprints.yaml**) est une partie important d'un thème ou du système de plugin. Ce fichier est essentiel pour le système GPM (Grav Package Manager). GPM utilises les informations contenues dans le dessein afin de mettre à disposition le plugin pour les utilisateurs.

Dans cet [exemple de dessein pour un plguin](example-plugin-blueprint), nous explorons en détail le dessein du plugin **Assets**. Ce dessein défini le nom, les informations sur l'auteur, les mots clé, la page d'acceuil, le lien pour remonter des bug, ainsi que d'autres metadonnées, qui nont seulement permettent à Grav de savoir où sont localisés les fichiers de mise à jour pour le plugin, mais définissent aussi des ressources utiles pour l'utilisateur et visible dans le module d'Administration de Grav

Uenf ois que ces informations sont données, un peu plus bas dans le page du Dessein, vous pouvez trouvez les informations sur le formulaire. Ces informations créées les formulaires d'Administration qui sont accessibles par l'utilisateur dans le "backoffice" de Grav. Par exemple, si vous voulez ajouter un bouton de type poussoir qui active ou désactive une fonctionnalité particulière d'un plugin, vous pouvez le définir à cet endroit.

![Admin Forms](blueprints_1.png?classes=shadow)

Le fichier **blueprints.yaml** fonctionne avec le fichier YAML rattaché au plugin (exemple: pour le plugin assets ; **assets.yaml**). Le dessein défini ce que sont les options de configurations, et le fichier YAML de la ressource correpondante définit leur valeurs. C'est ce fichier YAML qui va ensuite être dupliqué dans l'instance de Grav section : `user/config` pour surcharger les valeurs par défauts soit manuellement soit via l'administration de Grav

Pour résumer, quand on parle d'option de configuration pour un thème ou un plugin, le fichier **blueprints.yaml** le défini, and le fichier YAML portant le même nom que le plugin ou le thème détermine ses valeurs.

#### Pages

Une page Grav peut être tout ce que vous voulez. Une page peut être une liste d'article de blog, un article d'un blog, une page produit, une gallerie d'image, etc.

Ce qui défini ce que sera une page et comment elle sera affichée est le **Dessein de le Page**.

Grav défini quelques Dessein de page basique: défault (NdT: Defaut) et modulaire (Ndt: Modular). Ce sont les deux blocs de construction disponibles dans Grav.

Des Desseins de page additionnels sont ajoutés et défini par le thème, qui peut décider d'ajouter autant de Desseins de page que possible ou se focaliser sur des dessein de Page particulier pour réaliser ce qu'ils veulent obtenir.

Un thème Grav est bien plus flexible et puissant que ce que vous pouvez trouver sur d'autres plateformes.

Cela permet de définir des thèmes spécifiques à un type d'application. Par exemple, un thème peut se spécialiser dans un de ces objectifs: 

- réaliser un site de documentation, tel que celui que vous lisez actuellement.
- réaliser un site e-commerce.
- réaliser un blog.
- réaliser un "portfolio".
