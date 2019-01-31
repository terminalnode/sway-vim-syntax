# sway-vim-syntax - syntax highlighting for sway config files

This repository only contains very minor changes from that of [mboughaba/i3config.vim](https://github.com/mboughaba/i3config.vim/), mainly just adding file type detection for sway and possibly adding in keywords that don't exist in i3 syntax. Feel free to submit bug reports if anything is missing and I will try to fix it, or pull requests if you've already figured it out. My attitude towards the project is to fix things as I go along, not to provide a polished product.

## Features

The original i3config does what a syntax highlighting would do and additionally provides some sort of syntax checking. If you end up with *Bold Red* lines in your i3 config file this would mean that your syntax is wrong or there is an issue in the plugin.

Issues or deficiencies in this with regards to sway will be patched as they come up.

### File type detection

There is no specific extension for i3 config file.
For auto detection, the recommended method is to rename your file to something like:

+ .config/sway/*

## Installation instructions

### Vundle

Install using [vundle](https://github.com/gmarik/Vundle.vim) by adding

```vim
Plugin 'terminalnode/sway-vim-syntax'
```

to .vimrc and run `:PluginInstall`.

> I use Vundle myself, the two steps below may not be fully correct,
you need to change them to fit your needs.

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
