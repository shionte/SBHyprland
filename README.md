# Step 1
```
sudo pacman -S wofi kitty freetype2 cava zsh git hyprlock hyprpaper waybar ttf-font-awesome otf-font-awesome ttf-jetbrains-mono obsidian pavucontrol feh ranger thunar meson nwg-look papirus-icon-theme fastfetch file powerline-fonts inetutils ttf-dejavu bluez bluez-utils blueman telegram-desktop vlc

# Clone and install yay (AUR helper)
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si

# Install additional AUR packages
yay -S hyprshot wlogout python-pywal16

```

# Step 2

**Add repos**

```
cd ~/Documents

# GTK theme
git clone https://github.com/vinceliuice/Graphite-gtk-theme.git

# SBHyprland configuration
git clone https://github.com/shionte/SBHyprland.git

```

# Step 3

**Copy config**

```
cd SBHyprland
cp -r kitty waybar wlogout wofi hypr fastfetch mako wallpaper cava ~/.config

cd Graphite-gtk-theme
./install.sh
```



# Step 4

**Zsh themes**

```
# Install Oh My Zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Install Powerlevel10k theme
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git \
  "${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k"

# Install plugins
git clone https://github.com/zsh-users/zsh-autosuggestions \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting


nvim ~/.zshrc

# Add or edit these lines:
ZSH_THEME="powerlevel10k/powerlevel10k"
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)

# Save and apply changes
source ~/.zshrc
chsh -s /bin/zsh

reboot
```
📝 Notes & Subscription
This setup is optimized for Hyprland and Arch Linux.
Some packages and configs are optional; tailor it to your needs.
Keep your system updated: sudo pacman -Syu.
⭐ Support & Updates: If you want updates or extra configs, consider following the repo or subscribing to official channels.
