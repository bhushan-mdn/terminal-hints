# terminal-hints
Some simple tips and tools to significantly ease and enhance your command-line interface (CLI) life, moving from basic usage to power-user efficiency. 🚀

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

---

## ✨ The Prompt & Appearance
Choose a prompt that is fast, informative, and visually appealing.

* **OMZ Themes First:** Start with a clean, fast built-in OMZ theme (like `robyrussel` or `agnoster`) before adding more complexity.
* **Power Prompts (The Alternatives):**
    * **[Powerlevel10k](https://github.com/romkatv/powerlevel10k):** Extremely popular, highly configurable, and blisteringly fast Zsh theme. A must-try for many.
    * **[starship](https://starship.rs/):** A cross-shell, minimalist prompt that is fast and context-aware (shows Git branch, language versions, exit codes, etc.).

---

## 🚀 Efficiency Through Customization
The real power of the terminal comes from streamlining repetitive tasks.

### Aliases vs. Functions
* **Aliases:** Use for simple command replacements (e.g., `alias ls='ls -lah'`).
    * **OMZ Plugin Aliases:** Utilize aliases provided by OMZ plugins (e.g., the `git` plugin provides shortcuts like `gs` for `git status`).
* **Functions:** Use for a common **set of commands** or when you need to pass arguments or perform logic (e.g., a function to clone a repo and immediately `cd` into it).

### Environment Variables
* **Standardized Editor:** Define the `EDITOR` (or `VISUAL`) environment variable (e.g., `export EDITOR=nvim`). This allows you to use `\$EDITOR` in other aliases and scripts.
* **Contextual Editor:** Set your editor based on context, such as switching to a less resource-intensive editor (like `nano` or `vi`) when connected via **SSH** and reserving a full GUI-aware editor (like `nvim` or `code`) for local use.

### Directory Jumps
Stop typing full paths. Use a specialized tool for quick directory navigation:

* **[zoxide](https://github.com/ajeetds/zoxide) (Recommended) or `z`:** Learns your habits and lets you jump to frequently visited directories using minimal keywords.

---

## 🧑‍💻 Multiplexers & Session Management
Instead of relying on desktop-specific features like iTerm tabs, use a terminal multiplexer. This ensures a consistent environment regardless of whether you're local or SSH-ed into a server.

* **[tmux](https://github.com/tmux/tmux) or [Zellij](https://zellij.dev/):** Use these to manage multiple windows, panes, and persistent sessions within a single terminal window.

### tmux Workflow
* **Home Session on Startup:** Configure your `.zshrc` to automatically check for and attach to a "home" tmux session upon launching your terminal, otherwise creating it.
* **The Primeagen's Sessionizer:** Use a script like The Primeagen's **`tmux-sessionizer`** to quickly switch between or create new tmux sessions based on project directories.
    -   *Find it in The Primeagen's dotfiles repo.*

---

## 🛡️ Security and SSH
Streamline secure connections and password management.

* **SSH Agent Initialization:** Automatically start the `ssh-agent` upon shell login and load your private key to avoid typing your passphrase for every connection.
* **[Pass](https://www.passwordstore.org/) (The Standard Unix Password Manager):** For secure storage of sensitive credentials, integrate the `pass` utility.

---

## ⚙️Development
Tools that help with development

* `git-delta`: A viewer for Git diffs that enhances readability by providing syntax highlighting, side-by-side view, and robust paging. It makes reviewing code changes much easier directly in the terminal.

---

## 🔗 Inspiration & Dotfiles
Check out how experienced power-users configure their terminals and link them here to encourage exploration:

* **DistroTube's Dotfiles (GitLab):** Provides great examples of configuration for various window managers and terminal tools.
    -   https://gitlab.com/dwt1/dotfiles
* **Luke Smith's Dotfiles (GitHub):** Known for efficient, minimal, and keyboard-driven configurations.
    -   https://github.com/LukeSmithxyz/voidrice
* **ThePrimeagen's Dotfiles (GitHub):** Focuses on highly productive Neovim and tmux workflows.
    -   https://github.com/ThePrimeagen/.dotfiles
