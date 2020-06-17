# This page consists of the stuff I learned while solving the tmux room of tryhackme

[Link to the Clean TMUX Cheatsheet](https://imgur.com/bL9Dn3U)

tmux new -S SESSIONNAME - Spawn a new session

tmux a -t SESSIONNAME - Attach to an already existing tmux session

Do press the combo : CTRL + B , then release it, then press the keys to do stuff.
Eg, if you want to create a new window, press CTRL+B and release them, Then press C to Create a new window. Case insensitive.

CTRL+B is combo

combo  % - Split Vertically
combo  " - Split Horizontally
combo  [ - Enter Copy Mode
q	  - Exit Copy Mode
combo  ArrowKeys - Move from one pane to another
combo + ArrowKeys - Resize the current pane
combo x - Kill the current pane
