# terminal-> nvm command is not found in the zsh environment
This is my third day with MacBook, I found a problem yesterday.

After I install nvm, I enter "nvm -v" in the terminal, and the result show "nvm command not found".

### !!! The reason for this is that my terminal is zsh and I do not have `.zshrc` file.

so I new file and write `source ~/.bash_profile` at the end

```
touch .zshrc
open .zshrc
source .zshrc
```

____

if shell is not zsh and you want to use zsh, you can install oh-my-zsh 

curl install
> sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

wget install
> sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"



 if .bash_profile have problem
 
 Check file, If exists. Open file and copy this period of content
 ```
  export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

### check file
> `ls -a | grep <file>`
### check shell is zsh or bash
> `echo $SHELL`
### new file
> `touch <file>` or `vim <file>`

    

