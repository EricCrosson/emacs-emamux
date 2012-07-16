emamux.el
==================

Introduction
------------
*tmux* manipulation from Emacs. *emamux.el* is inspired by
[tslime.vim](https://github.com/kikijump/tslime.vim) and
[vimux](https://github.com/benmills/vimux/).

*WARNINGS: THIS IS ALPHA VERSION.*


Requirements
------------
* Emacs 22.1 or higher.
* tmux 1.6


Basic Usage
-----------

Send command to specified *target-session*(session:window.pane).
*target-session* is set as default at first `emamux:send-command` called.
If you change default *target-session*, you add `C-u` prefix.

    M-x emamux:send-command

Run command in a small split pane(`runner pane`) where emacs is in.

    M-x emamux:run-command

Move into the `runner pane` and enter the copy mode.

    M-x emamux:inspect-runner

Close `runner pane`.

    M-x emamux:close-runner-pane

Close all other panes in current window.

    M-x emamux:close-panes

Interrupt command which is running in `runner-pane`.

    M-x emamux:interrupt-runner

Clear tmux history in `runnerr-pane`

    M-x emamux:clear-runner-history


Customize
---------

Orientation of split pane, 'vertical or 'horizonal(Default is 'vertical).

    emamux:default-orientation

Height of `runner-pane`(Default is 20).

    emamux:runner-pane-height

Use nearest pane as `runner pane` instead of spliting pane(Default is nil).

    emamux:use-nearest-pane
