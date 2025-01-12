# Vim Commands

| Command                          | Description                                                              |
|----------------------------------|--------------------------------------------------------------------------|
| **Cursor movement**              |                                                                          |
| `h`                              | Move left                                                                |
| `j`                              | Move down                                                                |
| `k`                              | Move up                                                                  |
| `l`                              | Move right                                                               |
| `w`                              | Jump by start of words (punctuation considered words)                    |
| `W`                              | Jump by words (spaces separate words)                                    |
| `e`                              | Jump to end of words (punctuation considered words)                      |
| `E`                              | Jump to end of words (no punctuation)                                    |
| `b`                              | Jump backward by words (punctuation considered words)                    |
| `B`                              | Jump backward by words (no punctuation)                                  |
| `0`                              | Start of line                                                            |
| `^`                              | First non-blank character of line                                        |
| `$`                              | End of line                                                              |
| `G`                              | Go To command (prefix with number for specific line)                     |
| **Insert Mode**                  |                                                                          |
| `i`                              | Start insert mode at cursor                                              |
| `I`                              | Insert at the beginning of the line                                       |
| `a`                              | Append after the cursor                                                  |
| `A`                              | Append at the end of the line                                            |
| `o`                              | Open (append) blank line below current line                              |
| `O`                              | Open blank line above current line                                        |
| `ea`                             | Append at end of word                                                    |
| `Esc`                            | Exit insert mode                                                         |
| **Editing**                      |                                                                          |
| `r`                              | Replace a single character (does not use insert mode)                    |
| `J`                              | Join line below to the current one                                        |
| `cc`                             | Change (replace) an entire line                                          |
| `cw`                             | Change (replace) to the end of word                                       |
| `c$`                             | Change (replace) to the end of line                                       |
| `s`                              | Delete character at cursor and substitute text                           |
| `S`                              | Delete line at cursor and substitute text (same as `cc`)                 |
| `xp`                             | Transpose two letters (delete and paste, technically)                    |
| `u`                              | Undo                                                                     |
| `.`                              | Repeat last command                                                      |
| **Marking text (visual mode)**   |                                                                          |
| `v`                              | Start visual mode, mark lines, then do command (such as `y` for yank)    |
| `V`                              | Start linewise visual mode                                               |
| `o`                              | Move to other end of marked area                                         |
| `Ctrl+v`                         | Start visual block mode                                                  |
| `O`                              | Move to other corner of block                                            |
| `aw`                             | Mark a word                                                              |
| `ab`                             | A () block (with braces)                                                 |
| `aB`                             | A {} block (with brackets)                                               |
| `ib`                             | Inner () block                                                           |
| `iB`                             | Inner {} block                                                           |
| `Esc`                            | Exit visual mode                                                         |
| **Visual commands**              |                                                                          |
| `>`                              | Shift right                                                              |
| `<`                              | Shift left                                                               |
| `y`                              | Yank (copy) marked text                                                  |
| `d`                              | Delete marked text                                                       |
| `~`                              | Switch case                                                              |
| **Cut and Paste**                |                                                                          |
| `yy`                             | Yank (copy) a line                                                       |
| `2yy`                            | Yank 2 lines                                                             |
| `yw`                             | Yank word                                                                |
| `y$`                             | Yank to end of line                                                      |
| `p`                              | Put (paste) the clipboard after cursor                                    |
| `P`                              | Put (paste) before cursor                                                |
| `dd`                             | Delete (cut) a line                                                      |
| `dw`                             | Delete (cut) the current word                                            |
| `x`                              | Delete (cut) current character                                           |
| **Exiting**                       |                                                                          |
| `:w`                             | Write (save) the file, but don't exit                                    |
| `:wq`                            | Write (save) and quit                                                    |
| `:q`                             | Quit (fails if anything has changed)                                     |
| `:q!`                            | Quit and throw away changes                                              |
| **Search/Replace**               |                                                                          |
| `/pattern`                       | Search for pattern                                                       |
| `?pattern`                       | Search backward for pattern                                              |
| `n`                              | Repeat search in same direction                                          |
| `N`                              | Repeat search in opposite direction                                      |
| `:%s/old/new/g`                   | Replace all `old` with `new` throughout the file                        |
| `:%s/old/new/gc`                  | Replace all `old` with `new` throughout the file with confirmations      |
| **Working with multiple files**  |                                                                          |
| `:e filename`                    | Edit a file in a new buffer                                              |
| `:bnext (or :bn)`                | Go to next buffer                                                        |
| `:bprev (or :bp)`                | Go to previous buffer                                                    |
| `:bd`                             | Delete a buffer (close a file)                                           |
| `:sp filename`                   | Open a file in a new buffer and split window                             |
| `Ctrl+ws`                         | Split windows                                                            |
| `Ctrl+ww`                         | Switch between windows                                                   |
| `Ctrl+wq`                         | Quit a window                                                            |
| `Ctrl+wv`                         | Split windows vertically                                                 |

