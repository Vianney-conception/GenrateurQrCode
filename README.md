[![Translation status](https://vianneypacaud.fr/img/VIANNEYPACAUDBANIERE.svg)](https://vianneypacaud.fr/)

# Générateur de QR Code

Ce dépôt contient le code source d'une application web interactive permettant de générer et de personnaliser des QR Codes en haute résolution. L'application est accessible via [**qr-code.gervo.fr**](https://qr-code.gervo.fr).

## Structure du projet

- `index.html` : Fichier principal contenant la structure de l'interface utilisateur et la logique de navigation.
- `qr-code-styling.js` : Bibliothèque JavaScript utilisée pour le rendu, la stylisation et l'exportation des QR codes.
- `cdn.js` : Version locale du framework Tailwind CSS permettant un rendu visuel moderne et responsive.
- `.htaccess` : Configuration du serveur Apache gérant la réécriture d'URL, la redirection HTTPS et la gestion des erreurs 404/403 vers la page d'accueil.
- `logo.png` : Image par défaut utilisée pour l'identité visuelle du site.

## Fonctionnalités principales

- **Personnalisation du contenu** : Saisie dynamique d'URL ou de texte avec mise à jour en temps réel de l'aperçu.
- **Styles graphiques** : Personnalisation de l'apparence des points (carré, arrondi, etc.) et des coins du QR Code.
- **Gestion des couleurs** : Sélecteurs permettant de modifier la couleur principale et la couleur d'arrière-plan.
- **Logo central** : Possibilité d'importer un logo personnel pour l'insérer au centre du code généré.
- **Exports haute qualité** : Boutons d'exportation pour télécharger le résultat en format PNG (HD) ou en SVG (vectoriel) pour l'impression.

## Installation et utilisation

1. **Prérequis** :
   - Un navigateur web moderne.
   - Un serveur web Apache (optionnel, mais recommandé pour utiliser les règles du fichier `.htaccess`).

2. **Lancement** :
   - Clonez le dépôt ou téléchargez les fichiers.
   - Ouvrez directement le fichier `index.html` dans votre navigateur ou placez le dossier sur votre serveur.

## Points techniques

- **Confidentialité et RGPD** : Le générateur fonctionne exclusivement côté client (dans le navigateur). Aucune donnée saisie (URL, logos) n'est transmise ou stockée sur un serveur.
- **Performance** : Le chargement de Tailwind CSS via `cdn.js` permet une interface fluide sans dépendances externes lourdes au moment de l'exécution.
- **Réécriture d'URL** : Le fichier `.htaccess` assure que toutes les requêtes invalides ou sans extension pointent vers l'interface principale.

## Personnalisation

Le comportement par défaut du générateur (dimensions 2000x2000, couleurs par défaut, niveau de correction d'erreur 'Q') peut être ajusté directement dans la balise `<script>` du fichier `index.html` lors de l'instanciation de l'objet `QRCodeStyling`.

## Auteur

Projet développé par **Vianney Pacaud** (Vianney Conception).

---

**Licence :** Ce projet est Open Source. La reproduction totale ou partielle est autorisée.
