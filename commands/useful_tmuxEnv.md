# Set up plugins
In terminal:
```bash
mkdir -p ~/.tmux/plugins/{tpm,tmux-resurrect} 
cd .tmux
git clone https://github.com/tmux-plugins/tpm tpm
git clone https://github.com/tmux-plugins/tmux-resurrect tmux-resurrect
```
Then append to end of `~/.tmux.conf`:
```bash
# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'

# Other examples:
# set -g @plugin 'github_username/plugin_name'
# set -g @plugin 'git@github.com/user/plugin'
# set -g @plugin 'git@bitbucket.com/user/plugin'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run -b '~/.tmux/plugins/tpm/tpm'
```

Then run
```bash 
 tmux source ~/.tmux.conf 
```


Usage:
```
PREFIX + Ctrl+s (to save current session)
PREFIX + Ctrl+r (to restore last session)
```