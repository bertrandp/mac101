# mac101

## terminal

Pour installer fish sous macos (avec kubectl)

Dans l'ordre : 
- fish
- fisher
- kubectl
- tide
- créer les alias

### fish
`brew install fish`

### kubectl
setup kubectl

#### fisher 
https://github.com/jorgebucaran/fisher#installation
`curl -sL https://raw.githubusercontent.com/jorgebucaran/fisher/main/functions/fisher.fish | source && fisher install jorgebucaran/fisher`

#### tide

cf https://github.com/IlanCosman/tide#installation

Ne pas oublier les polices

### alias

#### git

Depuis https://gist.github.com/freewind/773c3324b5288ff636af
Créer un fichier `.config/fish/conf.d/git_aliases.fish` avec les alias :
```
# migrating from https://github.com/robbyrussell/oh-my-zsh/blob/master/plugins/git/git.plugin.zsh

# Aliases
alias g='git'
#compdef g=git
alias gst='git status'
#compdef _git gst=git-status
alias gd='git diff'
#compdef _git gd=git-diff
alias gdc='git diff --cached'
#compdef _git gdc=git-diff
alias gl='git pull'
#compdef _git gl=git-pull
alias gup='git pull --rebase'
#compdef _git gup=git-fetch
alias gp='git push'
#compdef _git gp=git-push
alias gd='git diff'

function gdv
  git diff -w $argv | view -
end

#compdef _git gdv=git-diff
alias gc='git commit -v'
#compdef _git gc=git-commit
alias gc!='git commit -v --amend'
#compdef _git gc!=git-commit
alias gca='git commit -v -a'
#compdef _git gc=git-commit
alias gca!='git commit -v -a --amend'
#compdef _git gca!=git-commit
alias gcmsg='git commit -m'
#compdef _git gcmsg=git-commit
alias gco='git checkout'
#compdef _git gco=git-checkout
alias gcm='git checkout master'
alias gr='git remote'
#compdef _git gr=git-remote
alias grv='git remote -v'
#compdef _git grv=git-remote
alias grmv='git remote rename'
#compdef _git grmv=git-remote
alias grrm='git remote remove'
#compdef _git grrm=git-remote
alias grset='git remote set-url'
#compdef _git grset=git-remote
alias grup='git remote update'
#compdef _git grset=git-remote
alias grbi='git rebase -i'
#compdef _git grbi=git-rebase
alias grbc='git rebase --continue'
#compdef _git grbc=git-rebase
alias grba='git rebase --abort'
#compdef _git grba=git-rebase
alias gb='git branch'
#compdef _git gb=git-branch
alias gba='git branch -a'
#compdef _git gba=git-branch
alias gcount='git shortlog -sn'
#compdef gcount=git
alias gcl='git config --list'
alias gcp='git cherry-pick'
#compdef _git gcp=git-cherry-pick
alias glg='git log --stat --max-count=10'
#compdef _git glg=git-log
alias glgg='git log --graph --max-count=10'
#compdef _git glgg=git-log
alias glgga='git log --graph --decorate --all'
#compdef _git glgga=git-log
alias glo='git log --oneline'
#compdef _git glo=git-log
alias gss='git status -s'
#compdef _git gss=git-status
alias ga='git add'
#compdef _git ga=git-add
alias gm='git merge'
#compdef _git gm=git-merge
alias grh='git reset HEAD'
alias grhh='git reset HEAD --hard'
alias gclean='git reset --hard; and git clean -dfx'
alias gwc='git whatchanged -p --abbrev-commit --pretty=medium'

#remove the gf alias
#alias gf='git ls-files | grep'

alias gpoat='git push origin --all; and git push origin --tags'
alias gmt='git mergetool --no-prompt'
#compdef _git gm=git-mergetool

alias gg='git gui citool'
alias gga='git gui citool --amend'
alias gk='gitk --all --branches'

alias gsts='git stash show --text'
alias gsta='git stash'
alias gstp='git stash pop'
alias gstd='git stash drop'

```

Pour le git tree, ajouter :
```
alias gt="git log --graph --date-order --date=short --pretty=format:'%C(auto)%h%d %C(reset)%s %C(blue)%aN %C(reset)%C(green)%cr' $argv;"
```

#### kubectl

Créer un fichier `.config/fish/conf.d/kubectl_aliases.fish` avec les alias :
```
alias k kubectl
alias kd 'k describe'
alias kg 'k get'
alias kaf 'k apply -f'
alias kdel 'k delete'
alias ke 'k edit'
alias kccc 'k config current-context'
alias kcdc 'k config delete-context'
alias kcsc 'k config set-context'
alias kcuc 'k config use-context'
alias kcgc 'k config get-contexts '
alias kdd 'kd deployment'
alias kdeld 'kdel deployment'
alias kdeli 'kdel ingress'
alias kdelp 'kdel pods'
alias kdels 'kdel svc'
alias kdelsec 'kdel secret'
alias kdi 'kd ingress'
alias kdp 'kd pods'
alias kds 'kd svc'
alias kdsec 'kd secret'
alias ked 'ke deployment'
alias kei 'ke ingress'
alias kep 'ke pods'
alias kes 'ke svc'
alias keti 'k exec -ti'
alias kgd 'kg deployment'
alias kgi 'kg ingress'
alias kgp 'kg pods'
alias kgrs 'kg rs'
alias kgs 'kg svc'
alias kgsec 'kg secret'
alias kl 'k logs'
alias klf 'k logs -f'
alias krh 'k rollout history'
alias krsd 'k rollout status deployment'
alias kru 'k rollout undo'
alias ksd 'k scale deployment'
```

## java et maven

### sdkman avec fish

https://github.com/sdkman/sdkman-cli#installation

https://github.com/reitzig/sdkman-for-fish

### java

`sdk list java`
`sdk install java x.y.z-tem`

### maven

`sdk install maven`
