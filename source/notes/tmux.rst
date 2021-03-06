tmux QOL settings
=================

tmux
----

.. code-block:: text

    # remap prefix from 'C-b' to 'C-a'
    unbind C-b
    set-option -g prefix C-a
    bind-key C-a send-prefix

    # split panes using | and -
    bind | split-window -h
    bind - split-window -v
    unbind '"'
    unbind %

    # switch panes using Alt-arrow without prefix
    bind -n M-Left select-pane -L
    bind -n M-Right select-pane -R
    bind -n M-Up select-pane -U
    bind -n M-Down select-pane -D

    # Enable mouse mode (tmux 2.1 and above)
    set -g mouse on

    # Bring cursor to beginning of line like in screen: C-a, a
    bind a send-prefix
