# github_helper

This is an ansible playbook that helps you(me) create a new git repository in your(my) Github via commandline using github's api key.


Instructions( a reminder to myself ):

Here is how you(I) set it up:

After clone, place the playbook and encrypted vault file under your(my) local bin directory

You(I) will need your(my) passcode in a file to allow the script to read the encrypted api key from the vaulted text under info.yml.

The vault text contains the api key for managing repo creation(only) on Github.

Create aliases under .bash_profile

alias gitrepo="cd $HOME/codes && ansible-playbook $HOME/.local/bin/gitrepo/gitrepo.yml --vault-password-file=$HOME/.vault_password_file" 
alias newrepo="cd $HOME/codes && ansible-playbook $HOME/.local/bin/gitrepo/gitrepo.yml --vault-password-file=$HOME/.vault_password_file" 
alias codes="cd $HOME/codes"
alias activate="$HOME/.local/bin/activate"

todo:
Create key rotation app or playbook for regular API key and vault password file update.
