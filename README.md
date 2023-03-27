# MochaTheme - MonoTheme GTK fork

> **Note** MochaTheme only includes Gnome Shell Theme, using Catppuccin (Lavender) colorscheme

## Preview:
![MochaTheme](https://user-images.githubusercontent.com/114978689/227776424-e5d5368a-f428-4170-97fe-6288fdab6f21.gif "Catppuccin Lavender From Ohio")
![Screenshot-Style4](https://user-images.githubusercontent.com/114978689/227846159-cb77e144-9f6f-45fd-aeef-830ce5c832c5.png "Using Aylur Widgets (Compact quick settings)")
![Screenshot-Style4](https://user-images.githubusercontent.com/114978689/227846177-39d9a26a-11dc-46c2-981b-2b650ee077ff.png)

## Installation:

**First, download or get files from the source:**

```sh
git clone --depth=1 https://github.com/lime-desu/MochaTheme.git ~/.local/share/themes/MochaTheme
```
Assuming the MochaTheme repo is stored on `~/.local/share/themes/`

> `~/.local/share/themes/` or `~/.themes` whichever you prefer

**Then create a symbolic link and store it on the proper directory:**
```sh
cd ~/.local/share/themes/MochaTheme && ln -sv $(pwd)/Mo* ../. # symlink all directories that begins with `Mo`
```
### Applying the theme:

> **Warning** [User Themes](https://extensions.gnome.org/extension/19/user-themes/) Extension is required.
	
#### Using `gsettings`

- Command = `gsettings set org.gnome.shell.extensions.user-theme name '<value>'`
- Value = `MochaTheme-<number>`, `MonoTheme`, and `MonoThemeDark`

```sh
gsettings set org.gnome.shell.extensions.user-theme name 'MochaTheme-4' # example using style4
```

> **Note** You can use this command for addding keybinding for changing style quickly, or even create a desktop application out of it.

#### Using `GNOME Tweaks`

1. Install and open GNOME Tweaks 
2. Click on the Appearance tab
3. Under "*Shell*", choose the desired style.

## Updating:

Since I suck at CSS, Expect some bugs that may need to update and to be fixed.
```sh
git -C pull --rebase ~/.local/share/themes/MochaTheme
```
## Uninstalling:

**Simply reverse the installation process**
```sh
rm -r ~/.local/share/themes/{Mocha*,Mono}Theme* # delete the repo and it's symlink
```

> **Note** **For MonoTheme and GTK app see below instructions**

<details>
<summary><h2> MonoTheme 👇</h2></summary>
    
# Mono Theme for Gnome
Simple theme with nothing extra to use on a regular basis. Theme tested on Manjaro and Fedora.  
The theme is still developing and it would be nice if you reported all the bugs in [issues.](https://github.com/witalihirsch/Mono-gtk-theme/issues)  

## Support
<div>
    <a href="https://www.patreon.com/witalihirsch">
        <img src="https://github.com/witalihirsch/Mono-gtk-theme/blob/main/images/patreon.png" width="250px" >
    </a>
</div>

## Mono Project Preview
<div>
    <a href="https://witalihirsch.github.io/mono.html">
        <img src="https://github.com/witalihirsch/Mono-gtk-theme/blob/main/images/monoproject.png" width="300px" >
    </a>
</div> 

## Mono Theme for Gnome
<p align="center"><b>Gtk4 apps</b></p>
<p align="center">
  <img alt="apps" src="https://github.com/witalihirsch/Mono-gtk-theme/blob/main/images/gtk4.png">
</p>

<p align="center"><b>Gtk3 apps</b></p>
<p align="center">
    <img alt="apps" src="https://github.com/witalihirsch/Mono-gtk-theme/blob/main/images/gtk3.png">
</p>

<p align="center"><b>Flatpak apps</b></p>
<p align="center">
    <img alt="flatpak" src="https://github.com/witalihirsch/Mono-gtk-theme/blob/main/images/flatpak.png">
</p>

<p align="center"><b>Gnome 43 apps</b></p>
<p align="center">
    <img alt="apps" src="https://github.com/witalihirsch/Mono-gtk-theme/blob/main/images/gnome43.png">
</p>

<p align="center"><b>Gnome-shell</b></p>
<p align="center">
    <img alt="apps" src="https://github.com/witalihirsch/Mono-gtk-theme/blob/main/images/gnome-shell.png">
</p>

## Wallpapers 
<p align="center"><b>Light</b></p>
<p align="center">
    <img alt="apps" src="https://github.com/witalihirsch/Mono-gtk-theme/blob/main/images/bg/Mono.png">
</p>

<p align="center"><b>Dark</b></p>
<p align="center">
    <img alt="apps" src="https://github.com/witalihirsch/Mono-gtk-theme/blob/main/images/bg/MonoDark.png">
</p>

## Download
Download theme [here.](https://github.com/witalihirsch/Mono-gtk-theme/releases)

## Installing
### GTK3 and Gnome-shell 
Move theme folders to `~/.themes`

### GTK4
To install the Gtk4 theme move the contents of `gtk4.0` to `~/.config/gtk4.0`

### Flatpak
To install themes on Flatpak apps use these commands:  
```pwsh
sudo flatpak override --filesystem=$HOME/.themes
```  
```pwsh
sudo flatpak override --env=GTK_THEME=MonoTheme
```
or
```pwsh
sudo flatpak override --env=GTK_THEME=MonoThemeDark
```

### GDM (optional)
IMPORTANT❗️ Take a snapshot of the system before use!  
If you want the gnome-shell theme to extend to the lock and login screen, move the `gnome-shell-theme.gresource` file from `gnome-shell` folder to `/usr/share/gnome-shell/` with a replacement and restart system with `ALT+F2` and enter `r` for Xorg or reboot/log out for Wayland session.  
Command:
```pwsh
sudo cp gnome-shell-theme.gresource /usr/share/gnome-shell
```  
I recommend saving the `gresource` file from the folder to a safe place beforehand, if will need to be returned. Go to /usr/share/gnome-shell and open terminal.  
Example:
```pwsh
sudo cp gnome-shell-theme.gresource ~/Documents
``` 

### Firefox
[Install Firefox Theme](https://github.com/witalihirsch/Mono-firefox-theme)

<p align="center"><b>Firefox</b></p>
<p align="center">
  <img alt="apps" src="https://github.com/witalihirsch/Mono-gtk-theme/blob/main/images/firefox.png">
</p>

### Icons
This is a mix of Adwaita symbolic icons and new icons that we made together with my friend. Icons match and don't get out from the style of Adwaita icons.  
[Install Icon Theme](https://github.com/witalihirsch/Mono-icon-theme)

<p align="center"><b>Icons</b></p>
<p align="center">
  <img alt="apps" src="https://github.com/witalihirsch/Mono-gtk-theme/blob/main/images/icons.png">
</p>

## Using
To change the light or dark theme of `Gtk3` apps and `Gnome-shell` use [Gnome Tweaks](https://gitlab.gnome.org/GNOME/gnome-tweaks) or [Night Theme Switcher](https://extensions.gnome.org/extension/2236/night-theme-switcher/) (choose the `MonoTheme` for day and `MonoThemeDark` for night variant in the `Themes` tab and change the theme color by switching style in Settings > `Appearance`).  
The dark and light appearance of Gtk4 is changed by renaming the desired file to `gtk.css` in `.config/gtk4.0` or you can try the script I made for automatic theme switcher in `gtk4` and `gtk3/4 flatpak` apps. Go to Night Theme Switcher and select `Commands` tab and paste this script.  
Sunrise:  
```pwsh
flatpak override --env=GTK_THEME=MonoTheme --user & cd ~/.config/gtk-4.0 ; mv gtk.css gtk2.css ; mv gtk-dark.css gtk.css ; mv gtk2.css gtk-dark.css
```
Sunset:  
```pwsh
flatpak override --env=GTK_THEME=MonoThemeDark --user & cd ~/.config/gtk-4.0 ; mv gtk.css gtk2.css ; mv gtk-dark.css gtk.css ; mv gtk2.css gtk-dark.css
```
Thanks to this script, you can change the theme of apps by switching dark and light theme in the settings, but gtk4 and gtk4 flatpak apps will be updated only when the app window is reopened. If `ALL` the steps are completed correctly, then the theme color will change for `ALL` applications in the system, write your questions in [issues.](https://github.com/witalihirsch/Mono-gtk-theme/issues)

## Uninstalling
To remove a theme, follow all the steps above in reverse order
</details>


