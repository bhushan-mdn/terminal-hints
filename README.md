# terminal-hints
Some simple tips and tools to significantly ease and enhance your command-line interface (CLI) life. 🚀

## 📚 Learning the Command Line
If you're looking to solidify your fundamental knowledge, check out these excellent resources:

* **The Art of Command Line:** A comprehensive guide to efficiency:
    - https://github.com/jlevy/the-art-of-command-line
* **Roadmap.sh - DevOps:** Specifically, look into the Process & Performance Monitoring, Networking, and Text Manipulation sections for powerful tools:
    - https://roadmap.sh/devops

---

## 🐚 The Shell & Framework (zsh + omz)
The first major step in leveling up your terminal is switching to a more modern and customizable shell like **Zsh**, managed by **Oh My Zsh** (OMZ).

**Step 1:** Install `zsh` and `oh-my-zsh` for managing plugins and configuration.

**Step 2:** Install these essential plugins. They provide syntax highlighting, smart history recall, and powerful fuzzy searching:

1.  **[zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting):** Provides instant feedback by highlighting valid and invalid commands *as you type*.
2.  **[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions):** Suggests commands based on your history, helping you finish long commands quickly.
3.  **fzf (Fuzzy Finder):** A versatile general-purpose fuzzy search tool. Use **`<Ctrl>-R`** for a powerful, searchable reverse history.
    * *Tip:* Ensure you source the key bindings and completion files after installing `fzf` to enable features like directory searching:
        ```bash
        source $HOME/.local/share/fzf/key-bindings.zsh
        source $HOME/.local/share/fzf/completion.zsh
        ```

---

## ✨ The Prompt (Aesthetics & Speed)
A clean, fast, and informative prompt is crucial for productivity.

* **starship:** A cross-shell, minimalist prompt that is incredibly fast and context-aware (shows Git branch, language versions, etc.).
    - https://starship.rs/
* *(Alternative:)* Consider using one of the lightweight built-in themes from Oh My Zsh, like `robyrussel`.

---

## 🛠️ Modern Utilities (Post-Modern CLI)
Replace older, less-efficient tools with their modern, faster, and more user-friendly counterparts.

* **ibraheemdev/modern-unix:** A curated list of excellent post-modern replacements for classic CLI utilities.
    - https://github.com/ibraheemdev/modern-unix

### Recommended Tools to Install:

* **`ripgrep` (`rg`):** The fastest recursive `grep` alternative.
* **`exa` or `lsd`:** Modern, colored replacements for `ls`.
* **`tldr`:** Community-driven, simplified man pages with examples.
* **`jq`:** A tool for slicing, filtering, mapping, and transforming JSON data.
