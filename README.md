# Neovim Setup

# Mac setup
1. Install Neovim
    ```bash
    brew install neovim
    ```
2. Install JetBrains Mono NerdFont
    ```bash
    brew tap homebrew/cask-fonts && brew install --cask font-jetbrains-mono-nerd-font
    ```
3. Install iTerm 2: https://iterm2.com
    - iTerm2 -> Settings -> Profiles -> Text
        - Check "Use a different font for non-ASCII text"
        - Select "JetbrainsMono Nerd Font"
4. Install Oh My ZSH: https://ohmyz.sh
    - Set the theme in `~/.zshrc`
    ```bash
    ZSH_THEME="amuse"
    ```
5. Install AstroNVim
    1. Remove previous installation of nvim (or save backup explained in next step)
    ```bash
    rm -rf ~/.config/nvim
    rm -rf ~/.local/share/nvim
    rm -rf ~/.cache/nvim
    ```
    2. Follow instructions: https://astronvim.github.io
6. Install GitHub Copilot
    ```bash
    git clone https://github.com/github/copilot.vim.git \
    ~/.vim/pack/github/start/copilot.vim
    ```
    ```bash
    nvim
    ```
    - This command will log you into the currently selected chrome browser profile github account
    ```bash
    :Copilot setup
    ```
7. Add custom user config at `~/.config/nvim/lua/user/init.lua`
    - [My custom config](./init.lua)
        - set number line to absolute
        - enable spell check
        - enable word wrap
        - added custom key `Space + fg` to search for exact word match
        - assigned key `ff` to the same function as the `<esc>` key
        - highlight selected line that cursor is on
        - enable copiloat autostart

# Ubuntu setup
1. 