# Setup

Add the following lines to ~/.zshrc:

```
ZSH_CONFIG_PATH="${HOME}/zsh-config"

if [ -d "$ZSH_CONFIG_PATH" ]; then
    git -C $ZSH_CONFIG_PATH pull --quiet
else
    mkdir -p "$(dirname $ZSH_CONFIG_PATH)"
    git clone https://github.com/JamesCarr1/zsh-config.git "$ZSH_CONFIG_PATH"
fi

source "$ZSH_CONFIG_PATH/.zshrc"
```

Feel free to edit `ZSH_CONFIG_PATH` to change where the repo is cloned
