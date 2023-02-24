# zsh_aliases
## Create An Alias In zsh Easy Guide

Aliases are a perfect choise to speed up your workflow by shorten commands to a few letters. <br>
In the following you'll find an easy and beginner friendly way to create your own Aliases in zsh.

## Show All Aliases
```bash
alias
```

## Delete An Alias
```bash
unalias <alias_name>
```

## Save Alias to .zshrc
To keep your aliases even after closing the terminal append them to .zshrc in you Home Directory and reopen a terminal to load the changes.
```bash
sudo vim ~/.zshrc
```

## Syntax Of An Alias
```bash
alias <alias_name>="<Command>; <command2>;echo [Note] && echo [Note2]"
```

## Go To Home Directory
```bash
alias home="cd ~/; echo Home Directory" 
```
In the terminal you only have to provide the alias_name to execute the command.
```bash
-$ home
```
## Listener On 443
```bash
alias rlw="sudo rlwrap nc -lvnp 443"
```

## Listener On <PORT_NUMBER>
You can create an alias with the argument $1.<br>
```bash
alias rlw="sudo rlwrap nc -lvnp $1"
```
Just type
```bash
-$ rlw 1234
```

## Open Server Port 80
```bash
alias server="echo python3 -c 'import pty;pty.spawn("/bin/bash")' && 
echo python -c 'import pty;pty.spawn("/bin/bash")' && 
echo script -qc /bin/bash /dev/null;
sudo python3 -m http.server 80"
```

## Open Server Port <PORT_NUMBER>
```bash
alias server="echo python3 -c 'import pty;pty.spawn("/bin/bash")' && 
echo python -c 'import pty;pty.spawn("/bin/bash")' && 
echo script -qc /bin/bash /dev/null;
sudo python3 -m http.server $1"
```
