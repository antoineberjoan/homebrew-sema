# Sema pour Mac

Vos repères économiques Webstat, à portée de main. Une app native pour les Mac avec puce Apple, sous macOS 14 ou version ultérieure.

Ce dépôt distribue le cask Homebrew et les versions binaires de Sema. Le code de l’application reste dans un dépôt privé.

## Télécharger

Les fichiers versionnés et leur empreinte SHA-256 sont disponibles dans les [Releases](https://github.com/antoineberjoan/homebrew-sema/releases).

Ouvrez le DMG, glissez Sema dans Applications, puis ouvrez l’app. L’accueil permet de choisir ses premiers repères, puis de connecter sa propre clé Webstat ou de découvrir la démonstration.

## Homebrew

```sh
brew install --cask antoineberjoan/sema/sema
```

Homebrew 7 peut demander d’approuver ce cask tiers. Après avoir consulté son contenu, utilisez :

```sh
brew trust --cask antoineberjoan/sema/sema
brew install --cask antoineberjoan/sema/sema
```

Pour une mise à jour : `brew upgrade --cask antoineberjoan/sema/sema`.

## Première ouverture

Cette alpha est signée localement et n’est pas notarisée par Apple. macOS peut bloquer sa première ouverture. Après une première tentative, vous pouvez autoriser cette app de confiance dans Réglages Système → Confidentialité et sécurité → Ouvrir quand même. Suivez la [procédure Apple](https://support.apple.com/fr-fr/102445). Homebrew conserve les contrôles macOS ; aucun script de contournement n’est fourni.

## Données et alertes

La clé personnelle Webstat est conservée dans le Trousseau du Mac et transmise uniquement à la Banque de France. Les préférences et les observations téléchargées restent locales. Aucune clé fournisseur partagée n’est distribuée.

Les alertes sont vérifiées lorsque vous actualisez les données dans Sema. Il n’y a pas de surveillance quand l’app est quittée ou le Mac en veille.
