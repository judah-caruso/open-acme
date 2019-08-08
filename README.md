Open Acme Scripts
-----------------

Open Acme Scripts is a repository of scripts to be used within the [Acme Editor](http://acme.cat-v.org/). Scripts are found in the `bin/` and, for the most part, require [Plan9Port](https://github.com/9fans/plan9port).


## Installation

To install all of the scripts, simple `git clone https://github.com/kyoto-shift/open-acme` and add the `open-acme/bin` to your `$PATH` like so: `export PATH=$PATH:[path-to-open-acme]/bin/`.

If you don't already have Acme or the Plan9Port setup on your machine, follow [this guide](https://github.com/9fans/plan9port) before downloading these scripts.


## Scripts

Below is a table of the scripts found in the `bin/` directory. | Filename                       | Script Name  | Description                                                                         | Arguments (? = optional)                                                                                                                                     | Example                   |
|--------------------------------|--------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| Commit                         | `commit`     | Automatically add and commit with Git/Mercurial.                                    | (?)`message` - A message to use for the current commit. If omitted, a commit message will be created using the current date and time.                        | `commit "initial commit"` |
| I+, I-                         | `i+`, `i-`   | Indent and unindent blocks of text.                                                 | (?)`size` - The number of spaces to use for the indention/unindention. `Default: 4`                                                                          | `|i+ 8`, `|i- 4`          |
| No Trailing Whitespace         | `ntw`        | Delete any trailing whitespace characters (`' '`, `'\t'`)                           | -                                                                                                                                                            | `|ntw`                    |
| Search                         | `s`          | Search through files using Ripgrep, The Silver Surfer, The Platinum Surfer, or Ack. | `query` - A search query to use with whichever editor is found.                                                                                              | `s foo`                   |
| Toggle Comments                | `tc`         | Toggle comments on the current selection.                                           | (?)`character` - Which character to use for the comment. Note: only use "non-enclosing" comment characters (e.g. `#`, `//`, etc.) `Default: //`              | `|tc '#'`                 |
| Spaces To Tabs, Tabs To Spaces | `stt`, `tts` | Convert tab characters to space characters (and vice versa).                        | (?)`level` - How many characters to use for the corresponding search. For example, `|stt 4` will convert every `4` spaces into a tab character. `Default: 4` | `|stt`, `|tts 4`          |


## Contribution

The best way to contribute is by helping create more scripts! If you have something you'd like to share, submit a pull request and let me know! Be sure to follow the style of the other files and to include a description of what your script(s) do (preferably in the source itself).