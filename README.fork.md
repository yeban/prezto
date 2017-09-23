### Personal fork of Prezto

#### Setup

```sh
git clone --recursive https://github.com/yeban/prezto.git "${ZDOTDIR:-$HOME}/.zprezto"

setopt EXTENDED_GLOB
for rcfile in "${ZDOTDIR:-$HOME}"/.zprezto/runcoms/^README.md(.N); do
  ln -s "$rcfile" "${ZDOTDIR:-$HOME}/.${rcfile:t}"
done
```

- Modify the `PATH` variable in `~/.zprofile`
- Min Zsh version 4.3.17

#### Updating

Run `zprezto-update` to automatically check if there is an update to zprezto.
If there are no file conflicts, zprezto and its submodules will be
automatically updated. If there are conflicts you will instructed to go into
the `$ZPREZTODIR` directory and resolve them yourself.

To pull the latest changes and update submodules manually:

```console
cd $ZPREZTODIR
git pull
git submodule update --init --recursive
```


#### Prompt themes

  1. For a list of themes, type `prompt -l`.
  2. To preview a theme, type `prompt -p name`.
  3. Load the theme in *~/.zpreztorc* then open a new Zsh terminal
     window or tab.


#### Resources

The [Zsh Reference Card][7] and the [zsh-lovers][8] man page are indispensable.

[7]: http://www.bash2zsh.com/zsh_refcard/refcard.pdf
[8]: http://grml.org/zsh/zsh-lovers.html
