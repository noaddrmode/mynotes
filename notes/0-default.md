# scrollbar fix
```
vim ~/.config/gtk-3.0/settings.ini

[Settings]
gtk-primary-button-warps-slider = false
```

# thunar fix
```
xfconf-query --channel thunar --property /misc-exec-shell-scripts-by-default --create --type bool --set true
```
