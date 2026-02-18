# fix-flatpak-theming
Specifically in Plasma 6

## Make theme dirs accessable
```sh
sudo flatpak override --filesystem=$HOME/.themes
```
```sh
sudo flatpak override --filesystem=$HOME/.icons
```
```sh
sudo flatpak override --filesystem=$HOME/.local/share/icons/
```
```sh
sudo flatpak override --filesystem=$HOME/.local/share/themes/
```

## Config stuff
```sh
sudo flatpak override --system --filesystem=xdg-config/gtk-3.0:ro --filesystem=xdg-config/gtkrc-2.0:ro --filesystem=xdg-config/gtk-4.0:ro --filesystem=xdg-config/gtkrc:ro
```
src: https://www.reddit.com/r/kde/comments/ujqih9/plasma_consistent_flatpak_theming/ 
## Fix action buttons in things like brave-browser
```sh
echo "@import 'window_decorations.css';" >> ~/.config/gtk-3.0/gtk.css
```
src: https://github.com/flathub/org.gtk.Gtk3theme.Breeze/issues/94#issuecomment-1499858638
