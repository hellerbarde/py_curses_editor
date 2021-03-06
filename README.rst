py_curses_editor  
================

Python curses text editor module. Provides a configurable pop-up window for
entering text, passwords, etc.

Posted by Scott Hansen <firecat4153@gmail.com>

Features:
---------
* Python 3.x
* Configurable window size and location
* Text box can have a title and/or an outlined box
* Text box can be initialized with existing text to edit
* Password mode for hiding text entries
* Pop-up help menu

Requires: 
---------

Python 3+

Installation:
-------------

* ``# python setup.py install``  OR
* ``$ python setup.py install --user``

License:
--------

* MIT

Usage:
------

From non-curses application::

    import editor
    editor.editor(box=False, inittext="Hi", win_location=(5, 5))

From curses application with a predefined curses window object (stdscr)::

    from editor.editor import Editor
    Editor(stdscr, win_size=(1,80), pw_mod=True, max_text_size=1)()

Keybindings:
------------

===================  =================================================
**F1**               Show popup help menu
**F2 or Ctrl-x**     Save and Quit
**Enter**            Enter new line, or Save and Quit (single line mode)
**F3 or ESC**        Cancel (no save)
**Cursor keys**      Movement
**Home/End**         Beginning or End of current line
**PageUp/PageDown**  PageUp/PageDown
**Delete**           Delete character under cursor
**Ctrl-k**           Delete to end-of-line
**Ctrl-u**           Delete to beginning-of-line
===================  =================================================

