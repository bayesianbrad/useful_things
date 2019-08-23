# Set up plugins
In terminal:
```bash
mkdir -p ~/.tmux/plugins/{tpm,tmux-resurrect} 
cd .tmux
git clone https://github.com/tmux-plugins/tpm tpm
git clone https://github.com/tmux-plugins/tmux-resurrect tmux-resurrect
```
Then append to end of `.tmux.conf`:
```bash
# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-resurrect'
```
Usage:
```
PREFIX + Ctrl+s (to save current session)
PREFIX + Ctrl+r (to restore last session)
```