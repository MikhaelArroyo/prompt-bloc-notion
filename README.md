# Générateur d'Idées de Prompts pour OBNL

Ce projet est une application web simple conçue pour aider les membres d'organismes à but non lucratif (OBNL) à générer des idées de prompts pour des outils d'intelligence artificielle comme ChatGPT ou Gemini.

## Comment l'utiliser

1.  Ouvrez le fichier `index.html` dans votre navigateur web.
2.  Sélectionnez une tâche dans le menu déroulant (par exemple, "Rédiger un courriel de remerciement").
3.  Cliquez sur le bouton "Générer un prompt".
4.  L'application affichera une suggestion de prompt que vous pouvez copier et adapter pour votre usage.

## Technologies utilisées

*   HTML5
*   [Tailwind CSS](https://tailwindcss.com/)
*   JavaScript (vanilla)

L'application appelle une API pour générer les prompts, qui utilise l'API de Google Gemini.

## Détails techniques

Quelques détails sur le fonctionnement interne de l'application :

*   **Proxy API** : Les appels à l'API de Google Gemini sont effectués via un proxy (un Cloudflare Worker). Cela permet de ne pas exposer de clés d'API directement dans le code côté client, renforçant ainsi la sécurité.
*   **Génération de prompt dynamique** : Le prompt envoyé à l'API n'est pas statique. Il est construit dynamiquement en JavaScript en fonction de la tâche sélectionnée par l'utilisateur, avec des instructions spécifiques pour garantir un format de réponse cohérent.
*   **Formatage Markdown** : La réponse de l'API est formatée en utilisant une fonction JavaScript simple qui convertit des balises de base (comme `**gras**` et `[[placeholder]]`) en HTML pour un affichage stylisé.

## À propos

Ce projet a été développé pour **La Puce Ressource Informatique**, un organisme communautaire qui vise à rendre la technologie accessible à tous.

[![Logo de La Puce Ressource Informatique](https://lapuce.org/new/wp-content/uploads/2024/03/cropped-VersionImpression.png)](https://lapuce.org)
