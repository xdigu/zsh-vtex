# Vtex Plugin

A simple zsh plugin to help with [vtex-cli commands](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-vtex-io-cli-command-reference#default-commands).

I strongly recommend that you use [you-should-use](https://github.com/MichaelAquilina/zsh-you-should-use) with this plugin that will remember all the aliases.

## Requirements

You should have vtex-cli to use this plugin, [see more here how to install](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-vtex-io-cli-install).

## Installation

Add one of the following to your .zshrc file depending on your package manager:

### [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh):

Copy this repository to `$ZSH_CUSTOM/custom/plugins`, where `$ZSH_CUSTOM` is the directory with custom plugins of oh-my-zsh [read more](https://github.com/robbyrussell/oh-my-zsh/wiki/Customization/):

```zsh
    git clone https://github.com/xdigu/zsh-vtex.git $ZSH_CUSTOM/plugins/vtex
```

Then add this line to your `.zshrc`. Make sure it is **before** the line `source $ZSH/oh-my-zsh.sh`.

```zsh
    plugins=(... vtex)
```

### Manual (Git Clone):

Clone this repository somewhere on your machine. This guide will assume `~/.zsh/zsh-vtex`.

```sh
    git clone https://github.com/xdigu/zsh-vtex.git ~/.zsh/zsh-vtex
```

Add the following to your `.zshrc`:

```sh
    source ~/.zsh/zsh-vtex/vtex.zsh
```

And then start a new terminal session.

## Aliases

| Alias                | Command                       | Description                                                                                                            |
| :------------------- | :---------------------------- | :--------------------------------------------------------------------------------------------------------------------- |
| vb                   | `vtex browse`                 | Opens the URL relative to your current workspace and account in a new browser window.                                  |
| vbqr                 | `vtex browse --qr`            | Same as browse but create a QR code of the url.                                                                        |
| vd                   | `vtex deploy`                 | Publishes an app as a stable version. Only works for apps previously published as a release candidate version.         |
| vil                  | `vtex install`                | Installs an app on the current workspace. If not specified which one, it defaults to the app in the current directory. |
| vl                   | `vtex link`                   | Syncs the app in the current directory with the development workspace in use.                                          |
| vlc                  | `vtex link --clean`           | Same as link and cleans builder cache.                                                                                 |
| vlv                  | `vtex link --verbose`         | Same as link and show all commands.                                                                                    |
| vlcv or vlvc         | `vtex link --clean --verbose` | Same as link , cleans builder cache and show all commands.                                                             |
| vls                  | `vtex list`                   | Lists the apps installed on the current workspace and account.                                                         |
| vlin                 | `vtex login`                  | Logs in to a VTEX account.                                                                                             |
| vlout                | `vtex logout`                 | Logs out of the current VTEX account.                                                                                  |
| vp                   | `vtex publish`                | Publishes the app in the current directory as a release candidate version.                                             |
| vs                   | `vtex switch`                 | Switches to another VTEX account.                                                                                      |
| vu                   | `vtex unlink`                 | Unlinks an app from the current workspace.                                                                             |
| vua                  | `vtex unlink --all`           | Unlinks all the apps from the current workspace.                                                                       |
| vwd {workspace name} | `vtex workspace delete`       | Deletes one or many workspaces from the current account.                                                               |
| vwu {workspace name} | `vtex workspace use`          | Creates and switches to a new workspace or simply switches to an existing one.                                         |

## Contributing

Pull requests and Feedback are welcome! 🎉
