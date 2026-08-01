# homebrew-claudy

Tap Homebrew de [Claudy](https://github.com/Endikk/Claudy) — le widget de bureau qui affiche
les quotas et la consommation Claude en temps réel.

Ce dépôt ne contient que la formule d'installation. Le code source vit dans
[Endikk/Claudy](https://github.com/Endikk/Claudy).

## Installation

```bash
brew install --cask Endikk/claudy/claudy
```

Homebrew ajoute le tap automatiquement à la première installation. Pour le faire à la main :

```bash
brew tap Endikk/claudy
brew install --cask claudy
```

## Mise à jour

```bash
brew upgrade --cask claudy
```

## Désinstallation

```bash
brew uninstall --cask claudy          # retire l'application
brew uninstall --zap --cask claudy    # retire aussi les préférences et le cache
```

## Publier une nouvelle version

À chaque release de Claudy, mettre à jour `version` **et** `sha256` dans
[`Casks/claudy.rb`](Casks/claudy.rb) :

```bash
shasum -a 256 dist/Claudy-<version>.zip
```

Le `sha256` doit toujours rester épinglé — jamais `:no_check`. C'est la seule vérification
d'intégrité de la chaîne de distribution, et le cask retire la quarantaine Gatekeeper après
installation.

## Licence

MIT — voir [Endikk/Claudy](https://github.com/Endikk/Claudy/blob/main/LICENSE).
