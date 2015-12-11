# Setup a new Ubuntu machnie

### Install ZSH shell


### Setup X forwarding
vim ~/.ssh/config
Adding the AddressFamily inet directive for, in this case, all hosts
<pre><code>
Host *
    ForwardAgent yes
    AddressFamily inet
</code></pre>
