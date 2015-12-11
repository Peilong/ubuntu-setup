# Setup a new Ubuntu machnie

### Install ZSH shell
1. Install ZSH
<pre><code>sudo apt-get install zsh</code></pre>
2. Set zsh as the default shell
<pre><code>chsh -s /bin/zsh</code></pre>
3. Install git
<pre><code>sudo apt-get install git</code></pre>
4. Install oh-my-ZSH
<pre><code>wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh
</code></pre>
5. Edit .zshrc file: vim ~/.zshrc
<pre><code>alias cls='clear'
alias ll='ls -l'
alias la='ls -a'
alias vi='vim'
alias javac="javac -J-Dfile.encoding=utf8"
alias grep="grep --color=auto"
</code></pre>
6. Change robbyrussell theme
<pre><code>vim ~/.oh-my-zsh/themes/robbyrussell.zsh-theme</code></pre>
Change "c" current directory to "d" absolute directory as following:
<pre><code>PROMPT='%{$fg_bold[red]%}➜ %{$fg_bold[green]%}%p %{$fg[cyan]%}%d %{$fg_bold[blue]%}$(git_prompt_info)%{$fg_bold[blue]%} % %{$reset_color%}'
</code></pre>
7. Restart machine

### Setup X forwarding
vim ~/.ssh/config
Adding the AddressFamily inet directive for, in this case, all hosts
<pre><code>Host *
    ForwardAgent yes
    AddressFamily inet
</code></pre>
