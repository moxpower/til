# Git Command Line Tricks

## See the branch and status in your bash prompt

There are two things to add to your `.bashrc`. One makes it so that you can see two things: 

 - the branch you are in
 - the current state of the git repo that you are in.

Example: 

```bash
# jonathan (master)*$
```

the *(master)* is added to my bash prompt when I am in a folder that is a git repo. The \* means that there are uncommitted changes in the repo. 

I add the following code to my `.bashrc` so that I remember the steps to install (commented), and how to add it. As you're downloading code from the internet be sure to double check that it's doing what you expect/hope before blindly running it. 

```bash
# mkdir ~/.bash
# cd ~/.bash
# git clone git://github.com/jimeh/git-aware-prompt.git
# Check the code to make sure it's doing what you want!
export GITAWAREPROMPT=~/.bash/git-aware-prompt
source $GITAWAREPROMPT/main.sh
```

## Autocomplete commands

You can tab complete to complete available git commands and branches in a context aware way! I mean that you can do obvious things like: 

`$ git stat<TAB>` and it will complete into `git status` (or give you options if it's ambiguous). That's nice but it really comes in handy when you can: `$ git push origin jonathan_exp<TAB>` and it will even complete the full branch name: `$ git push origin jonathan_experimental_long_branch_name`. 

Add the following to explain where you got the code and the instructions for how to install it: 

```bash
# curl https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash -o ~/.git-completion.bash
# Check the code to make sure it's doing what you want!
if [ -f ~/.git-completion.bash ]; then
  . ~/.git-completion.bash
fi
```
