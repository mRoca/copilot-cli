---
title: "completion"
linkTitle: "completion"
weight: 9
---

```
$ copilot completion [shell] [flags]
```

### What does it do?
`copilot completion` prints shell completion code for bash or zsh. The code must be evaluated to provide interactive completion of commands.

See the help menu for instructions on how to setup auto-completion for your respective shell.

### What are the flags?
```bash
-h, --help   help for completion
```

### Examples
Install zsh completion.
```bash
$ source <(copilot completion zsh)
$ copilot completion zsh > "${fpath[1]}/_copilot" # to autoload on startup
```
Install bash completion on macOS using homebrew.
```bash
$ brew install bash-completion   # if running 3.2
$ brew install bash-completion@2 # if running Bash 4.1+
$ copilot completion bash > /usr/local/etc/bash_completion.d
```
Install bash completion on linux
```bash
$ source <(copilot completion bash)
$ copilot completion bash > copilot.sh
$ sudo mv copilot.sh /etc/bash_completion.d/copilot
```