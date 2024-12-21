# Dotfiles JetBrains settings sync

A temporary workaround for syncing JetBrains IDE settings on Gitpod automatically until it's officially supported (https://youtrack.jetbrains.com/issue/IJPL-13075/Support-Settings-Sync-with-the-remote-development)

Also see the relevant Gitpod docs here: https://www.gitpod.io/docs/references/ides-and-editors/pycharm#configure-ide-settings-per-user

## Quickstart

1. Fork this repository to your own account ([direct link](https://github.com/gitpod-samples/dotfiles_jetbrains_settings/fork))
2. Go to https://gitpod.io/user/preferences and scroll down. (You may replace `gitpod.io` with your own instance domain)
3. Copy your forked repo link and set it as **Dotfiles - Repository URL** and click on `Save`.
4. Create new workspace to see in action.
5. Make your settings modifications in JetBrains IDE (e.g. Pycharm) settings.
6. `Find Action` (⇧ + ⌘ + A) > `Restart IDE` to save the IDE changes to disk. (**Very Important**)
7. Open a terminal and run `commitjb` to save/update your persistent settings.

As such, all your new workspaces will use your saved settings. If you need to sync new changes, just redo 6. & 7.

Keep in mind that this will sync individual IDE settings. If you ran `commitjb` from Pycharm, those settings will be only applied to Pycharm IDEs, not other JetBrains IDEs. If you want to apply generic settings across all JetBrains IDEs you can manually commit them to `$HOME/.dotfiles/home_files/.gitpod/jetbrains/options` dir.
