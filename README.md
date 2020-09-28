# sway-vim-syntax - syntax highlighting for sway config files

This repository only contains very minor changes from that of [mboughaba/i3config.vim](https://github.com/mboughaba/i3config.vim/), mainly just adding file type detection for sway, changing behaviour for keywords that are used differently in sway and adding keywords that don't exist in i3.

Contrary to the original repo I do not aim to provide full coverage of all config syntax, but rather to fix issues as they pop up for me. Bug reports and pull requests are welcome however.

## Features

The original i3config does what a syntax highlighting would do and additionally provides some sort of syntax checking. If you end up with *Bold Red* lines in your i3 config file this would mean that your syntax is wrong or there is an issue in the plugin.

Issues or deficiencies in this with regards to sway will be patched as they come up. It should work fine with i3 as well seeing as it was originally written for it (though you'd have to edit ftdetect), but no effort will be spent on maintaining compatibility. 

### File type detection

There is no specific extension for sway config file. For auto detection, put the file in a folder structure ending in .config/sway (I suggest ~/.config/sway). Note that you can have multiple files in this folder if you wish to split your config into different files and use `include` to import them.

## Installation instructions

### Vundle

Install using [vundle](https://github.com/gmarik/Vundle.vim) by adding

```vim
Plugin 'terminalnode/sway-vim-syntax'
```

to .vimrc and run `:PluginInstall`.

> I use Vundle myself, the two steps below may not be fully correct,
you need to change them to fit your needs.

### Vim-Plug

Install using [vim-plug](https://github.com/junegunn/vim-plug) by adding

```vim
Plug 'terminalnode/sway-vim-syntax'
```

to .vimrc or neovim init.vim and running `:PlugInstall`

### Git submodule + Pathogen

If you have [pathogen](https://github.com/tpope/vim-pathogen) installed,
and you prefer to use git submodules, run

```sh
cd ~/.vim
git submodule add https://github.com/terminalnode/sway-vim-syntax.git bundle/syntax/
```

### Manual installation

If you don't have either Vundle or Pathogen installed, copy both i3config.vim file
to .vim/after/syntax and .vim/after/ftdetect respectively.

```sh
git clone https://github.com/terminalnode/sway-vim-syntax.git /tmp/sway-vim-syntax
mkdir -p ~/.vim/after/syntax/
mv /tmp/i3config.vim/after/syntax/sway-vim-syntax ~/.vim/after/syntax/sway-vim-syntax
rm -rf /tmp/i3config.vim
```

## Inspired by
+ mboughaba/i3config.vim
 <https://github.com/mboughaba/i3config.vim> (Where almost all the code is from)
+ PotatoesMaster/i3-vim-syntax
  <https://github.com/PotatoesMaster/i3-vim-syntax>
+ vim-scripts/edifact.vim
  <https://github.com/vim-scripts/edifact.vim> (For Error highlighting).

## License

MIT
