# tmux---complete-guidline-Beginner-to-Advanced-
This repository contains a step-by-step guide for tmux, starting from installation up to advanced usage. It is designed for both beginners and advanced users.




🔹 Step 1: Installation  


On Ubuntu/Debian:  
```
sudo apt update && sudo apt install tmux -y  
```
On Fedora/CentOS:
```
sudo dnf install tmux -y
```
Check installed version:
```
tmux -V
```

🔹 Step 2: Session Management

👉 A session is like a container where your terminal environment runs.

Start a new session:  
```
tmux
```
  
Start with a custom name:
```
tmux new -s mysession
```
List all sessions:
```
tmux ls
```
Attach to a session:
```
tmux attach -t mysession
```
Detach from a session (keep running in background):
```
Ctrl+b d
```
Kill a session:
```
tmux kill-session -t mysession
``` 


🔹 Step 3: Window Management

👉 A window is like a tab inside a session.

New window → Ctrl+b c  
List windows → Ctrl+b w  
Next window → Ctrl+b n  
Previous window → Ctrl+b p  
Switch to window by number → Ctrl+b <number>  
Rename window → Ctrl+b ,  
Kill window → Ctrl+b &  


🔹 Step 4: Pane Management  

👉 Split a window into multiple panes.  

Split vertically → Ctrl+b "  
Split horizontally → Ctrl+b %  
Switch between panes → Ctrl+b + Arrow keys  
Resize pane → Ctrl+b (hold) + Arrow keys  
Swap panes → Ctrl+b { or Ctrl+b }  
Kill a pane → Ctrl+b x  


🔹 Step 5: Copy & Paste Mode  

Enter copy mode → Ctrl+b [  
Move cursor → Arrow keys  
Start selection → Space  
Copy → Enter  
Paste →  Ctrl+b ]  


🔹 Step 6: Scrolling & History  

Enter scroll mode → Ctrl+b [  
Use Arrow keys or PgUp/PgDn  


🔹 Step 7: Configuration (~/.tmux.conf)  

You can customize tmux by editing ~/.tmux.conf.  

👉Example configuration:  

Use Ctrl+a instead of Ctrl+b  
unbind C-b  
set-option -g prefix C-a  
bind-key C-a send-prefix  

👉Enable mouse support  
set -g mouse on  

👉Status bar customization  
set -g status-bg black  
set -g status-fg green  
set -g status-left "#S "  
set -g status-right "%H:%M %d-%b-%y"  


Reload configuration:  
tmux source-file ~/.tmux.conf  


🔹 Step 8: Quick Cheat Sheet  

New session → tmux new -s name  
Detach → Ctrl+b d  
List sessions → tmux ls  
Attach → tmux attach -t name  
New window → Ctrl+b c  
Rename window → Ctrl+b ,  
Split vertically → Ctrl+b "  
Split horizontally → Ctrl+b %  
Switch pane → Ctrl+b + Arrow  
Kill pane → Ctrl+b x  
Copy mode → Ctrl+b [  


🔹 Conclusion  
tmux is a powerful tool that allows you to manage multiple terminal sessions, windows, and panes efficiently.
By learning its basics and advanced features, you can significantly improve productivity in Linux environments.


##  Resources

You can download the full guide in PDF format:  

- [tmux Complete Guideline (Beginner to Advanced) — PDF](tmux%20-%20complete%20guidline.pdf)  

