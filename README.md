# get-started
the few things to do to get started with git, node, npm

# git

for an in depth introduction, check this out 
- https://github.com/auremoser/git-intro

set email and authors variables

https://help.github.com/articles/setting-your-username-in-git/

```
git config --global user.name "your name" # it does not matter
git config --global user.email "YOUR EMAIL ADDRESS" # same as your github email
```

Check also,
- this guideline to manage your privacy https://help.github.com/articles/keeping-your-email-address-private/
- https://help.github.com/articles/setting-your-username-in-git/

# ssh

```
ssh-keygen -t rsa -b 4096 -C GH-USERNAME@users.noreply.github.com
cat ~/.ssh/id_rsa.pub # copy paste it to github, 
# alternatively you may use 
# cat ~/.ssh/id_rsa.pub| xclips
ssh -T git@github.com # accept the new host, then ensure it welcome you with your GH username
```

# node

Consider using nvm https://github.com/creationix/nvm

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh | bash
# new terminal
nvm install 5.0
nvm use 5.0
```

- https://github.com/creationix/nvm

# npm

```
npm config set init.author.name "your name"
npm config set init.author.email "your email"
npm config set init.license MIT
```

To choose the most appropriate licence for your work, consider to take a look at http://choosealicense.com/

# suggestion

I suggest you this snippet alias to start a module,

```sh
alias npi='npm init -y && git init && touch .gitignore && touch index.js && mkdir test && touch README.md && touch test/index.js'
```
