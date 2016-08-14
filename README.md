# slimline

Minimal, fast and elegant ZSH prompt. Displays the right information at the right time.

Features:
- sleek look
- asynchronous git information display using a custom python script
- the prompt symbol is colored red, when all asynchronous tasks are finished it turns white
- exit code of last command if the exit code is not zero
- runtime of executed command if it exceeds a threshold
- username and host name if connected to a ssh server

![](screenshot.png)

With all information (connected to ssh server, runtime and exit status from last command):
![](screenshot_full.png)

## Requirements

* zsh

## Optional

* python 2.7+ to enable git information display

## Installation

Choose one of the methods below.

### [antigen](https://github.com/zsh-users/antigen)

```
antigen bundle mgee/slimline
```

### [zgen](https://github.com/tarjoilija/zgen)

```
zgen load mgee/slimline
```

### Manually

Clone the repository:

```git clone --recursive https://github.com/mgee/slimline.git```

Source the prompt in your `.zshrc` (or other appropriate) file:

```source <path-to-slimline>/slimline.zsh```

## Options

### `SLIMLINE_PROMPT_SYMBOL`

Defines the symbol of the prompt. Default is `∙`.

### `SLIMLINE_EXIT_STATUS_SYMBOL`

Defines the symbol of the exit status glyph. Default is `↵`.

### `SLIMLINE_DISPLAY_EXEC_TIME`

Defines whether the runtime of a process is displayed if it exceeds the maximum execution time
specified by the option below. Default is `1`.

### `SLIMLINE_MAX_EXEC_TIME`

Defines the maximum execution time of a process until its run time is displayed on exit.
Default is `5` seconds.

### `SLIMLINE_DISPLAY_EXIT_STATUS`

Defines whether the exit status is displayed if the exit code is not zero. Default is `1`.

### `SLIMLINE_DISPLAY_SSH_INFO`

Defines whether the `user@host` part is displayed if connected to a ssh server. Default is `1`.

### `SLIMLINE_ENABLE_GIT`

Defines whether git information shall be displayed (requires python). Default is `1`.

### `SLIMLINE_GIT_REPO_INDICATOR`

Defines the git repository indicator text. Default is `%fᚴ`.

### `SLIMLINE_GIT_NO_TRACKED_UPSTREAM`

Defines the text which is displayed if the branch has no remote tracking branch.
Default is `upstream %F{red}⚡%f`.

### `SLIMLINE_GIT_REMOTE_COMMITS_PUSH_PULL`

Defines the format used to display commits which can be pushed and pulled to/from `origin/master`.
Default is `𝘮 ${remote_commits_to_pull} %F{yellow}⇄%f ${remote_commits_to_push}`.

### `SLIMLINE_GIT_REMOTE_COMMITS_PULL`

Defines the format used to display commits which can be pulled from `origin/master`.
Default is `𝘮 %F{red}→%f${remote_commits_to_pull}`.

### `SLIMLINE_GIT_REMOTE_COMMITS_PUSH`

Defines the format used to display commits which can be pushed to `origin/master`.
Default is `𝘮 %F{green}←%f${remote_commits_to_push}`.

### `SLIMLINE_GIT_BRANCH`

Defines the format for the local branch. Default is `${branch}`.

### `SLIMLINE_GIT_DETACHED`

Defines the format if the repository is not on a branch. Default is `%F{red}detached@${sha1}%f`.

### `SLIMLINE_GIT_LOCAL_COMMITS_PUSH_PULL`

Defines the format used to display commits which can be pushed and pulled to/from the remote tracking
branch. Default is `${local_commits_to_pull} %F{yellow}⥯%f ${local_commits_to_push}`.

### `SLIMLINE_GIT_LOCAL_COMMITS_PULL`

Defines the format used to display commits which can be pulled from the remote tracking branch.
Default is `${local_commits_to_pull}%F{red}↓%f`.

### `SLIMLINE_GIT_LOCAL_COMMITS_PUSH`

Defines the format used to display commits which can be pushed to the remote tracking branch.
Default is `${local_commits_to_push}%F{green}↑%f`.

### `SLIMLINE_GIT_STAGED_ADDED`

Defines the format used to display staged added files. Default is `${staged_added}%F{green}A%f`.

### `SLIMLINE_GIT_STAGED_MODIFIED`

Defines the format used to display staged modified files. Default is `${staged_modified}%F{green}M%f`.

### `SLIMLINE_GIT_STAGED_DELETED`

Defines the format used to display staged deleted files. Default is `${staged_deleted}%F{green}D%f`.

### `SLIMLINE_GIT_STAGED_RENAMED`

Defines the format used to display staged renamed files. Default is `${staged_renamed}%F{green}R%f`.

### `SLIMLINE_GIT_STAGED_COPIED`

Defines the format used to display staged copied files. Default is `${staged_copied}%F{green}C%f`.

### `SLIMLINE_GIT_UNSTAGED_MODIFIED`

Defines the format used to display unstaged modified files. Default is `${unstaged_modified}%F{red}M%f`.

### `SLIMLINE_GIT_UNSTAGED_DELETED`

Defines the format used to display unstaged deleted files. Default is `${unstaged_deleted}%F{red}D%f`.

### `SLIMLINE_GIT_UNTRACKED`

Defines the format used to display untracked files. Default is `${untracked}%F{white}A%f`.

### `SLIMLINE_GIT_UNMERGED`

Defines the format used to display unmerged files. Default is `${unmerged}%F{yellow}U%f`.

### `SLIMLINE_GIT_STASHES`

Defines the format used to display the number of stashes. Default is `${stashes}%F{yellow}≡%f`.

## Thanks to

- [sindresorhus/pure](https://github.com/sindresorhus/pure)
- [sorin-ionescu/prezto](https://github.com/sorin-ionescu/prezto.git)
- [michaeldfallen/git-radar](https://github.com/michaeldfallen/git-radar)
- [gbataille/gitHUD](https://github.com/gbataille/gitHUD)

## License

Released under the [MIT License](LICENSE)
