# Dotfiles Repository

This repository contains my personal configuration files (**dotfiles**) for setting up and maintaining a consistent development environment across different machines.

## 📁 What’s Inside?
This repo includes configurations for:
- **Shell** (e.g., `.bashrc`, `.zshrc`)
- **Git** (e.g., `.gitconfig`)
- **Neovim/Vim** (e.g., `.vimrc`, `nvim/init.vim`)
- **Terminal & Prompt** (e.g., `.tmux.conf`, `.p10k.zsh`)
- **Other Tools** (e.g., `.config/`, `.aliases`)

## 🔄 Installation & Setup

### 1️⃣ Clone the Repository
```sh
git clone https://github.com/sarkargourab/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
```

### 2️⃣ Backup Existing Dotfiles (Optional but Recommended)
```sh
mkdir -p ~/dotfiles_backup
mv ~/.bashrc ~/.zshrc ~/.vimrc ~/.gitconfig ~/dotfiles_backup/ 2>/dev/null
```

### 3️⃣ Use GNU Stow to Symlink Dotfiles
```sh
stow bash  # Example: Stow bash configs
stow nvim  # Stow Neovim configs
stow git   # Stow Git configs
```

### 4️⃣ Reload Shell & Apply Changes
```sh
source ~/.bashrc   # For Bash
source ~/.zshrc    # For Zsh
```

## 🔧 Adding New Dotfiles
1. Add new configurations inside the appropriate folder.
2. Run `stow <folder_name>` to create symlinks.
3. Commit and push changes:
   ```sh
   git add .
   git commit -m "Added new config for <tool>"
   git push origin main
   ```

## 🛠 Restoring Dotfiles on a New Machine
```sh
git clone https://github.com/sarkargourab/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
stow *
```

## ✨ Customization
Feel free to modify the configurations based on your workflow.

---
📌 **Tip:** Keep your dotfiles updated and version-controlled to ensure a seamless dev setup anywhere! 🚀

