# sema pour Mac

Vos repères économiques Webstat, à portée de main. Une app native pour les Mac avec puce Apple, sous macOS 14 ou version ultérieure.

Ce dépôt distribue le cask Homebrew et les versions binaires de sema. Le [code de l’application](https://github.com/antoineberjoan/sema) est public sous licence MIT.

## Télécharger

Les fichiers versionnés et leur empreinte SHA-256 sont disponibles dans les [Releases](https://github.com/antoineberjoan/homebrew-sema/releases).

Ouvrez le DMG, glissez sema dans Applications, puis ouvrez l’app. L’accueil permet de choisir ses premiers repères, puis de connecter sa propre clé Webstat ou de découvrir la démonstration.

## Homebrew

Sur un nouveau Mac, préparez le tap et approuvez uniquement ce cask après l’avoir consulté :

```sh
brew tap antoineberjoan/sema
brew trust --cask antoineberjoan/sema/sema-app
```

Puis installez sema :

```sh
brew install --cask sema-app
```

Installation directe sans préparation séparée : `brew install --cask antoineberjoan/sema/sema-app`.
Mise à jour : `brew upgrade --cask sema-app`. Le renommage depuis l’ancien cask `sema` est déclaré dans `cask_renames.json`.

La commande courte utilise ce tap tiers ; sema n’est pas référencée dans le catalogue officiel Homebrew. Les protections de macOS restent applicables.

## Première ouverture

Cette alpha est signée localement et n’est pas notarisée par Apple. macOS peut bloquer sa première ouverture. Après une première tentative, vous pouvez autoriser cette app de confiance dans Réglages Système → Confidentialité et sécurité → Ouvrir quand même. Suivez la [procédure Apple](https://support.apple.com/fr-fr/102445). Homebrew conserve les contrôles macOS ; aucun script de contournement n’est fourni.

## Données et alertes

La clé personnelle Webstat est conservée dans le Trousseau du Mac et transmise uniquement à la Banque de France. Les préférences et les observations téléchargées restent locales. Aucune clé fournisseur partagée n’est distribuée.

Les repères sont actualisés toutes les 24 h tant que sema tourne, même avec le hub fermé. Le lancement et le réveil contrôlent leur fraîcheur ; seules les données devenues anciennes sont récupérées. Les alertes suivent les nouvelles observations. Commande R force une actualisation. Il n’y a pas de surveillance quand l’app est quittée ou le Mac en veille.
