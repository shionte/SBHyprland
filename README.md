# 🌌 SBHyprland Setup Guide

A complete step-by-step guide to set up **Hyprland** with custom configs, GTK themes, Zsh, and essential tools on Arch Linux.

---

## 📦 Step 1

**Install Packages**

```bash
sudo pacman -S wofi kitty freetype2 cava zsh git hyprlock hyprpaper waybar ttf-font-awesome otf-font-awesome ttf-jetbrains-mono obsidian pavucontrol feh ranger thunar meson nwg-look papirus-icon-theme fastfetch file powerline-fonts inetutils ttf-dejavu bluez bluez-utils blueman vlc

# Clone and install yay (AUR helper)
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si

# Install additional AUR packages
yay -S hyprshot wlogout python-pywal16
```

# 🌐 Step 2

**Add Repositories / Themes**

```
cd ~/Documents

# GTK theme
git clone https://github.com/vinceliuice/Graphite-gtk-theme.git

# SBHyprland configuration
git clone https://github.com/shionte/SBHyprland.git

```

# 📋Step 3

**Copy configs to ~/.config**

```
cd SBHyprland
cp -r kitty waybar wlogout wofi hypr fastfetch wallpaper cava ~/.config

cd Graphite-gtk-theme
./install.sh
```



# ⚙️Step 4

**Setup Zsh and Powerlevel10k**

```
# Install Oh My Zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Install Powerlevel10k theme
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git "${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k"

# Install plugins
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

**Edit your .zshrc**
```
nvim ~/.zshrc

# Add or edit these lines:
ZSH_THEME="powerlevel10k/powerlevel10k"
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)

# Save and apply changes
source ~/.zshrc


reboot
```

# 💡Tips
🎨 Optional Tweaks
Wallpaper & Cava visualizer already included in configs.
Customize waybar, kitty, wofi, mako, and other configs in ~/.config.

📝 Notes & Subscription
This setup is optimized for Hyprland and Arch Linux.
Some packages and configs are optional; tailor it to your needs.
Keep your system updated: sudo pacman -Syu.
⭐ Support & Updates: If you want updates or extra configs, consider following the repo or subscribing to official channels.
