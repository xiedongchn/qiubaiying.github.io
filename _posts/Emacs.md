## Hot Keys

**Copy line:**

```
C-a C-SPACE C-n M-w C-y
```

which breaks down to

- `C-a`: move cursor to start of line
- `C-SPACE`: begin a selection ("set mark")
- `C-n`: move cursor to next line
- `M-w`: copy region
- `C-y`: paste ("yank")

The aforementioned

```
C-a C-k C-k C-y C-y
```

amounts to the same thing (TMTOWTDI)

- `C-a`: move cursor to start of line
- `C-k`: cut ("kill") the line
- `C-k`: cut the newline
- `C-y`: paste ("yank") (we're back at square one)
- `C-y`: paste again (now we've got two copies of the line)

These are both embarrassingly verbose compared to `C-d` in your editor, but in Emacs there's always a customization. `C-d` is bound to `delete-char` by default, so how about `C-c C-d`? Just add the following to your `.emacs`:

```
(global-set-key "\C-c\C-d" "\C-a\C- \C-n\M-w\C-y")
```

Beware: some Emacs modes may reclaim `C-c C-d` to do something else.

**Copy selected text and paste:**

- To cut the text, press `C-w`.
- To copy the text, press `M-w`.
- To paste the text, press `C-y`.

**Look for help:**
`C-h f`:will look for help for specific functions.

`M-x where-is RET goto-line RET`: list the bindings for the command `goto-line`.

`C-h b`: which lists all the bindings for the current buffer (and then you can peruse the bindings to see if `goto-line` is there, or to discover other useful commands & bindings.

**Goto line:**

`M-g g` or `M-g M-g` are the default bindings for `goto-line`.

And, the easiest way to find this is either `M-x where-is RET goto-line RET` which will list the bindings for the command `goto-line`, or you can type `C-h b` which lists all the bindings for the current buffer (and then you can peruse the bindings to see if `goto-line` is there, or to discover other useful commands & bindings.

**New File:**
`M-!` to enter shell command, then `touch <filename>` to make the file.