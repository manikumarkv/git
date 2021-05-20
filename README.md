# 1.Remove all local branches which are not availabe in origin

Create a aliase for easy access

``` git
git config --global alias.gone "! git fetch -p && git for-each-ref --format '%(refname:short) %(upstream:track)' | awk '\$2 == \"[gone]\" {print \$1}' | xargs -r git branch -D"
```
and run alias

``` git
git gone
```
# 2. pull from different branch (Ex:master)

```git
git pull origin master
```
