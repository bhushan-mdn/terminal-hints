# terminal-hints
Some simple tips to make your cli life easier.

If you want to learn about using the command line use one of the following:
- https://github.com/jlevy/the-art-of-command-line
- https://roadmap.sh/devops (Go through the Process & Performance Monitoring, Networking and Text Manipulation tools sections)

## zsh
Step 1: Install zsh and oh-my-zsh (nickname: omz) for managing plugins.
Step 2: Install the following plugins which are really useful:
1. [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting) (Syntax highlighting for your commands
2. [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
3. fzf (for reverse history search and directory, file search - great thing is it's all fuzzy).
   Usually I source them directly after installing fzf.
   ```
   source $HOME/.local/share/fzf/key-bindings.zsh
   source $HOME/.local/share/fzf/completion.zsh
   ```

## starship (maybe just use robyrussel from omz)
A minimalist shell prompt theme.  
https://starship.rs/

## More
- [ibraheemdev/modern-unix](https://github.com/ibraheemdev/modern-unix) - Post-modern replacements for commonly used cli utilities.
