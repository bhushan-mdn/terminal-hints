# terminal-hints
Some simple tips and tools to significantly ease and enhance your command-line interface (CLI) life, moving from basic usage to power-user efficiency. 🚀

[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/bhushan-mdn/terminal-hits) 
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) 
[![Built With](https://img.shields.io/badge/Built%20With-Zsh%2Ftmux%2Ffzf-blue.svg)]()

## 📚 Learning the Command Line
If you're looking to solidify your fundamental knowledge, check out these excellent resources:

* **The Art of Command Line:** A comprehensive guide to efficiency:
    -   https://github.com/jlevy/the-art-of-command-line
* **Roadmap.sh - DevOps:** Specifically, look into the Process & Performance Monitoring, Networking, and Text Manipulation sections for powerful tools:
    -   https://roadmap.sh/devops

---

## 🐚 The Shell & Framework (Zsh + Oh My Zsh)
Switching to **Zsh**, managed by **Oh My Zsh** (OMZ), is the foundation for a highly customizable and efficient terminal.

### Essential Plugins
Install the following via OMZ (or manually) for a massive quality-of-life improvement:

1.  **[zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting):** Provides instant feedback by highlighting valid and invalid commands *as you type*.
2.  **[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions):** Suggests commands based on your history, helping you finish long commands quickly.
3.  **fzf (Fuzzy Finder):** A versatile general-purpose fuzzy search tool. Use **`<Ctrl>-R`** for a powerful, searchable reverse history.
    * *Tip:* Ensure you source the key bindings and completion files after installing `fzf`:
        ```bash
        source $HOME/.local/share/fzf/key-bindings.zsh
        source $HOME/.local/share/fzf/completion.zsh
        ```

### 🧠 History Management & Context
Maximize your history to maintain context across sessions:

* **Absurdly High History:** Set the `HISTSIZE` and `SAVEHIST` variables in your `.zshrc` to a very large number (e.g., `1000000`) so you never lose your command history.
* **[Atuin](https://atuin.sh/):** A modern, SQLite-backed shell history replacement that records more context and supports cross-machine synchronization.

### ⌨️ VI Mode for Shell Editing
For powerful command-line editing, set your shell to use **VI keybindings**. This allows you to navigate and edit commands using the highly efficient `hjkl` and other VI motions, often faster than using arrow keys and Home/End.
    ```bash
    # Add this to your .zshrc or .bashrc
    bindkey -v
    ```

---

## ✨ The Prompt & Appearance

### Prompt Themes
Choose a prompt that is fast, informative, and visually appealing.

* **OMZ Themes First:** Start with a clean, fast built-in OMZ theme (like `robyrussel` or `agnoster`) before adding more complexity.
* **Power Prompts (The Alternatives):**
    * **[Powerlevel10k](https://github.com/romkatv/powerlevel10k):** Extremely popular, highly configurable, and blisteringly fast Zsh theme. A must-try for many.
    * **[starship](https://starship.rs/):** A cross-shell, minimalist prompt that is fast and context-aware (shows Git branch, language versions, exit codes, etc.).

### 🎨 Aesthetics & Fonts
* **⚠️ Mandatory Font:** To display the icons and glyphs used by modern power prompts and utilities, you *must* install a **Nerd Font** (e.g., Meslo, FiraCode, or Hack patched with glyphs).

---

## 🚀 Efficiency Through Customization
The real power of the terminal comes from streamlining repetitive tasks.

### Aliases vs. Functions
* **Aliases:** Use for simple command replacements (e.g., `alias ls='ls -lah'`).
    * **OMZ Plugin Aliases:** Utilize aliases provided by OMZ plugins (e.g., the `git` plugin provides shortcuts like `gs` for `git status`).
        * These references would be handy, just learn the most commonly used.
            * https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/git
            * https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/systemd
            * https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/docker
* **Functions:** Use for a common **set of commands** or when you need to pass arguments or perform logic (e.g., a function to clone a repo and immediately `cd` into it).
    * e.g. `function gclg() { git clone github.com/google/$1 }` Usage: `gclg uuid` 

### Environment Variables
* **Standardized Editor:** Define the `EDITOR` (or `VISUAL`) variable.
* **Contextual Editor:** Set your editor based on context using logic in your `.zshrc`:
    ```bash
    # Use a minimal editor over SSH, full editor otherwise.
    if [ -z "$SSH_CLIENT" ]; then
      export EDITOR=nvim
    else
      export EDITOR=vi
    fi
    ```

### Directory Jumps
Stop typing full paths. Use a specialized tool for quick directory navigation:

* **[zoxide](https://github.com/ajeetds/zoxide) (Recommended) or `z`:** Learns your habits and lets you jump to frequently visited directories using minimal keywords.

---

## ⚙️ Utilities & Text Processing
Replace older, less-efficient tools with their modern, faster, and more user-friendly counterparts.

* **[ibraheemdev/modern-unix](https://github.com/ibraheemdev/modern-unix):** A curated list of excellent post-modern replacements for classic CLI utilities.

### Navigation & File Inspection
* **[bat](https://github.com/sharkdp/bat):** A `cat` clone with syntax highlighting, Git integration, and automatic paging.
* **[nnn](https://github.com/jarun/nnn):** A minimalist yet powerful file manager with VI-like keybindings.
* **`ripgrep` (`rg`):** The fastest recursive `grep` alternative, built to respect `.gitignore` rules.
* **[tldr](https://tldr.sh/):** Provides community-driven, simplified man pages with practical usage examples.

### Data & System Tools
* **`jq`** and **`yq`:** The definitive command-line processors for **JSON** and **YAML** respectively.
* **[hurl](https://hurl.dev/):** A command-line tool that runs HTTP requests defined in a simple text format—great for testing APIs.
* **[procs](https://github.com/dalance/procs):** A modern, readable, and colored alternative to the classic `ps` command.
* **[duf](https://github.com/muesli/duf):** A user-friendly replacement for `df` to view disk space usage.
* **[sd](https://github.com/chmln/sd):** A fast, user-friendly replacement for `sed` that makes simple string replacements easy.

---

## 💻 Development Workflow

* **`git-delta`:** A viewer for Git diffs that enhances readability by providing syntax highlighting, side-by-side view, and robust paging.
* **[asdf](https://asdf-vm.com/):** A version manager for handling multiple runtime versions (Node.js, Python, Ruby, etc.) with a single, consistent tool.
* **`shellcheck`:** Use this static analysis tool to write robust, reliable, and secure shell scripts.

---

## 🧑‍💻 Multiplexers & Session Management
Use a terminal multiplexer for a consistent environment, especially on remote servers.

* **[tmux](https://github.com/tmux/tmux) or [Zellij](https://zellij.dev/):** Manage multiple windows, panes, and persistent sessions.

### Tmux Workflow
* **Home Session on Startup:** Configure your `.zshrc` to automatically check for and attach to a "home" tmux session upon launching your terminal.
* **The Primeagen's Sessionizer:** Use a script like The Primeagen's **`tmux-sessionizer`** to quickly switch between or create new tmux sessions based on project directories.
    -   *Find it in The Primeagen's dotfiles repo.*

---

## 🛡️ Security and SSH
Streamline secure connections and password management.

* **SSH Agent Initialization:** Automatically start the `ssh-agent` upon shell login and load your private key to avoid typing your passphrase for every connection.
* **[Pass](https://www.passwordstore.org/) (The Standard Unix Password Manager):** For secure storage of sensitive credentials, integrate the `pass` utility.

---

## 🔗 Inspiration & Dotfiles
Check out how experienced power-users configure their terminals and link them here to encourage exploration:

* **DistroTube's Dotfiles (GitLab):** Provides great examples of configuration for various window managers and terminal tools.
    -   https://gitlab.com/dwt1/dotfiles
* **Luke Smith's Dotfiles (GitHub):** Known for efficient, minimal, and keyboard-driven configurations.
    -   https://github.com/LukeSmithxyz/voidrice
* **ThePrimeagen's Dotfiles (GitHub):** Focuses on highly productive Neovim and tmux workflows.
    -   https://github.com/ThePrimeagen/.dotfiles

---

## 🌐 Community & Discovery (Subreddits)

These subreddits are excellent resources for finding new tools, seeing creative terminal setups ("ricing"), and discussing command-line efficiency.

* **r/unixporn:** Focused on aesthetic customization of UNIX-like environments (including terminals and shells). This is where you'll find the best color schemes and prompt configurations.
* **r/commandline:** A general discussion forum for command-line efficiency, scripts, utilities, and general workflow tips.
* **r/vim** / **r/neovim:** If you are serious about text editing within the terminal, these communities are essential for configuration and advanced usage.
* **r/devops:** Often features discussions on advanced automation, scripting, and server management tools.
