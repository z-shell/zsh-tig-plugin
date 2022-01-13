<h2 align="center">
  <a href="https://github.com/z-shell/zi">
    <img src="https://github.com/z-shell/zi/raw/main/docs/images/logo.svg" alt="Logo" width="80" height="80" />
  </a>
❮ ZI ❯ Plugin - Zsh Tig
</h2> 

- [Introduction](#introduction)
- [The Added Bindings](#the-added-bindings)
  - [—— Make Bindings ——](#-make-bindings-)
    - [xmf – eXecute MakeFile](#xmf--execute-makefile)
    - [xamf – eXecute `all` MakeFile](#xamf--execute-all-makefile)
    - [xcmf – eXecute `clean` MakeFile](#xcmf--execute-clean-makefile)
  - [—— Copy Bindings ——](#-copy-bindings-)
    - [xcp - eXecute CoPy](#xcp---execute-copy)
    - [xfcp - eXecute File CoPy](#xfcp---execute-file-copy)
  - [—— Editor Bindings ——](#-editor-bindings-)
    - [xed - eXecute EDitor](#xed---execute-editor)
    - [xled - eXecute List EDitor](#xled---execute-list-editor)
  - [—— Midnight Commander Bindings ——](#-midnight-commander-bindings-)
    - [xmc – eXecute Midnight Commander](#xmc--execute-midnight-commander)
    - [xhmc – eXecute Home Midnight Commander](#xhmc--execute-home-midnight-commander)
- [Installation](#installation)
  - [ZI](#zi)
  - [Zinit](#zinit)
  - [Antigen](#antigen)
  - [Oh-My-Zsh](#oh-my-zsh)
  - [Zgen](#zgen)

## Introduction

A plugin for Zsh that automatically adds a few advanced bindings and also
provides a Zsh-rewritten function and/or script `tig-pick` (i.e.: the code is
agnostic and can be run either as a script or as a function; it defaults to
function), originally shipped with tig as `sh`-script in the `contrib/`
subdirectory.

## The Added Bindings

### —— Make Bindings ——

#### xmf – eXecute MakeFile

Retrieves the list of targets for `Makefile` in the current directory and runs
`fzf` or `fzy` on the list and then, when a target gets selected, executes
`make` on that target.

#### xamf – eXecute `all` MakeFile

Runs `make all`

#### xcmf – eXecute `clean` MakeFile

Runs `make clean`

### —— Copy Bindings ——

#### xcp - eXecute CoPy

Copies the SHA of currently active (highlighted) commit into the clipboard.
Supports OS X's `pbcopy` and Linux/other's `xsel` and `xclip`.

#### xfcp - eXecute File CoPy

Copies the contents of currently active (highlighted) file into the clipboard.
Supports OS X's `pbcopy` and Linux/other's `xsel` and `xclip`.

### —— Editor Bindings ——

#### xed - eXecute EDitor

Executes an editor on selected file. It's either `$VISUAL`, then `$EDITOR` and
then `vim`.

#### xled - eXecute List EDitor

Runs fuzzy-finder (either `fzf` or `fzy`) on the list of the files in the
repository and after selecting one it then executes an editor like in `xed`.

### —— Midnight Commander Bindings ——

#### xmc – eXecute Midnight Commander

Executes `mc` with the left pane set to the repository and the right pane to
`$ZSH_TIG_MC_DIR`. If the variable isn't set it uses `$HOME` instead.

#### xhmc – eXecute Home Midnight Commander

Executes `mc` with the left pane set to the repository and the right pane to the
home directory.

## Installation


### [ZI](https://github.com/z-shell/zi)

Add `zi load z-shell/zsh-tig-plugin` to your `.zshrc` file. Zinit will
clone the plugin the next time you start zsh. To update issue `zi update
z-shell/zsh-tig-plugin`.

```zsh
zi load z-shell/zsh-tig-plugin
```

Or with use of the Turbo mode:

```zsh
zi wait lucid for z-shell/zsh-tig-plugin
```

### Zinit

```zsh
zinit load z-shell/zsh-tig-plugin
```

### Antigen

Add `antigen bundle z-shell/zsh-tig-plugin` to your `.zshrc` file. Antigen will
handle cloning the plugin for you automatically the next time you start zsh.

```zsh
antigen bundle z-shell/zsh-tig-plugin
```

### Oh-My-Zsh

1. `cd ~/.oh-my-zsh/custom/plugins`
2. `git clone git@github.com:z-shell/zsh-tig-plugin.git`
3. Add `zsh-tig-plugin` to your plugin list

### Zgen

Add `zgen load z-shell/zsh-tig-plugin` to your .zshrc file in the same place
you're doing your other `zgen load` calls in.

<!-- vim:set ft=markdown tw=80 fo+=a1n autoindent: -->
