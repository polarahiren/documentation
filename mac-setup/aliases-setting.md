# Aliases setting

- Open terminal
- Create Aliases file with below command:
   ````
   vim ~/.aliases
   ````
- Press `i` for insert text
- Add your aliases that you're using daily. 
  i.g.,
  ````
    alias gs="git status"
    alias gl="git log"
    alias gcom="git checkout master"
    alias gaa="git add ."
    alias gc="git commit -m "
    alias gp="git push"
    alias nah="git reset --hard && git clean -df"
    alias gb="git branch"
    alias home="cd ~"
    alias code="cd ~/code"
    alias c="clear"
    alias ..="cd .."
    alias copyssh="pbcopy < ~/.ssh/id_rsa.pub"
    alias ci="composer install"
    alias yi="yarn"
    alias watch="yarn run watch"
    alias hot="yarn run hot"
    alias yi-dev="yarn && yarn run dev"
    alias yi-watch="yarn && yarn run watch"
    alias laravel-echo="laravel-echo-server start"
    alias clear-compiled="php artisan clear-compiled"
    alias cachec="php artisan cache:clear"
    alias configc="php artisan config:clear"
    alias routec="php artisan route:clear"
    alias viewc="php artisan view:clear"
    alias optimize="php artisan optimize:clear"
    alias art="php artisan"
    alias mfs="php artisan migrate:fresh --seed"
    alias migrate="php artisan migrate"
    alias rollback="php artisan migrate:rollback"
    alias tinker="php artisan tinker"
    alias seed="php artisan db:seed"
    alias ide-helpers="php artisan ide-helper:generate && php artisan ide-helper:meta && php artisan ide-helper:models -N"
    alias cda="composer dump-autoload"
    alias setup="git pull && ci && yi && yarn run dev && mfs && ide-helpers"
  ````
  
-    Save and quit file with below command
     - click `ESC`
     - press `:wq`
- Add the following to your `.zshrc`: 
    ````
    source ~/.aliases
    ````
- Start a new terminal session.
