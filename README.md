# hyprland-dotfiles

Repo contenant l'ensemble des dotfiles que j'utilise dans ma configuration Hyprland.

Voici les dépendances nécessaires à son fonctionnement :

 - Hyprland
 - Hyprpaper
 - Waybar
 - Kitty
 - Nerd Fonts (https://github.com/ryanoasis/Nerd-Fonts)

Vous référez à la documentation de ces paquets ou au wiki d'Hyprland : https://wiki.hyprland.org/Getting-Started/Installation/

## Hyprland

J'utilise également le plugin split-monitor-workspaces afin d'avoir un comportement proche de DWM (avec 10 workspaces par écran) : https://github.com/Duckonaut/split-monitor-workspaces

Voici comment l'activer :

```
hyprpm update
hyprpm add https://github.com/Duckonaut/split-monitor-workspaces # Add the plugin repository
hyprpm enable split-monitor-workspaces # Enable the plugin
hyprpm reload # Reload the plugins
```

Pour la partie configuration, il vous suffit de mettre le fichier `hyprland.conf` dans votre `~/.config/hypr/` et celui-ci détectera automatiquement celle-ci.
Cette configuration tient compte que vous avez un clavier AZERTY.

De plus, une configuration sera nécessaire pour la partie gestion de vos écrans, toujours situé dans le fichier `hyprland.conf` :

```
monitor = DP-3, 3440x1440@165, 1920x0, 1
monitor = HDMI-A-1, 1920x1080@60, 0x0, 1
```

Vous pouvez lister la configuration possible avec l'utilitaire `hyprctl` :

```hyprctl monitors all```

Voir https://wiki.hyprland.org/Configuring/Monitors/ au besoin.

## Waybar

Pour la configuration de Waybar, j'utilise celle fournit par défaut, avec quelques modifications sur les icônes utilisées.
Elle utilise les polices Nerd Fonts : https://github.com/ryanoasis/Nerd-Fonts 

Il suffit donc de mettre les fichiers `config.jsonc` et `style.css` dans `~/.config/waybar/`.

## Curseur

J'utilise le curseur Future Cyan Hyprcursor compatible avec l'outil hyprcursor disponible ici : https://gitlab.com/Pummelfisch/future-cyan-hyprcursor
L'installation de celui-ci y est décrite.

## Gestion des fonds d'écrans

L'utilitaire Hyprpaper convient à la gestion des wallpapers.
La configuration que j'utilise se situe dans le fichier `hyprpaper.conf` qu'il faudra placer dans `~/.config/hypr/`.

Le lancement de l'outil se fait directement par Hyrpland à l'aide d'un `exec-once`.
