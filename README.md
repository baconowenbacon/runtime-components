# ~/.bashrc — read by bash every time you open an interactive terminal.
#
# After editing, apply your changes to the current terminal with:
#     source ~/.bashrc

# ---------------------------------------------------------------------------
# Stop here if this shell is not interactive.
# ---------------------------------------------------------------------------
# Programs like scp and rsync start a non-interactive bash behind the scenes.
# If this file prints anything in that situation, those programs break.
# This line makes everything below apply only when a human is typing.
[[ $- != *i* ]] && return

# ---------------------------------------------------------------------------
# History
# ---------------------------------------------------------------------------
HISTSIZE=10000              # commands remembered in this session
HISTFILESIZE=20000          # commands saved to ~/.bash_history
HISTCONTROL=ignoreboth      # skip duplicates and lines starting with a space
shopt -s histappend         # add to the history file instead of overwriting it

# ---------------------------------------------------------------------------
# Prompt:   user@host:~/cs240/hw1 (main)$
# ---------------------------------------------------------------------------
# Shows the current git branch when you are inside a repository.
git_branch() {
    local b
    b=$(git symbolic-ref --short HEAD 2>/dev/null) && printf ' (%s)' "$b"
}
idk what to put here #lol


