## add remote
git remote add ${name} ${url}  

## add config
git config --global user.name "${name}"  
git config --global user.email ${email}  

# set editor
git config --global core.editor vim  

# set colors
git config --global color.ui true  

## remove config global
git config --global --unset ${option}  

## revert commit unpublished
git reset --hard HEAD~${number}  

## pretty logs
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"  
