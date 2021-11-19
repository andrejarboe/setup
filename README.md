# setup

cd ~

mkdir code

sudo apt update

sudo apt install zsh -y

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"


git clone https://github.com/spaceship-prompt/spaceship-prompt "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1

ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme" 

## install mononoki fonts from nerdfonts https://www.nerdfonts.com/font-downloads


code ~/.zshrc

## #Put this on the bottom of file
SPACESHIP_PROMPT_ADD_NEWLINE="true" 
SPACESHIP_CHAR_SYMBOL=" \uf0e7" 
#SPACESHIP_CHAR_PREFIX="\uf296" 
SPACESHIP_CHAR_SUFFIX=(" ") 
SPACESHIP_CHAR_COLOR_SUCCESS="yellow" 
SPACESHIP_PROMPT_DEFAULT_PREFIX="$USER" 
SPACESHIP_PROMPT_FIRST_PREFIX_SHOW="true" 
SPACESHIP_USER_SHOW="true"

export LS_COLORS="di=34;40:ln=36;40:so=35;40:pi=33;40:ex=32;40:bd=1;33;40:cd=1;33;40:su=0;41:sg=0;43:tw=0;42:ow=34;40:"
zstyle ':completion:*:default' list-colors ${(s.:.)LS_COLORS}

export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm

## install nvm
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | zsh

or

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash



## copy terminal settings into windows terminal settings.json 

## Installing git

### step 1
sudo apt update

sudo apt upgrade


### step 2
sudo add-apt-repository ppa:git-core/ppa

sudo apt update

sudo apt install git

### step 2
git --version

## Configure
git config --global user.name "Andre Jarboe"

git config --global user.email "andrejarboe@gmail.com"

git config --global init.defaultBranch main

git config --global color.ui auto

## Verify
git config --get user.name

git config --get user.email

## Create an SSH Key
ls ~/.ssh/id_rsa.pub

ssh-keygen -C andrejarboe@gmail.com

##  Link Your SSH Key with GitHub

cat ~/.ssh/id_rsa.pub

Highlight and copy the output, which starts with ssh-rsa and ends with your email address.

Now, go back to GitHub in your browser window and paste the key you copied into the key field. Then, click Add SSH key. You’re done! You’ve successfully added your SSH key!

## Test it

testing