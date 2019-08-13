### Run all this
```
brew install nvm
mkdir ~/.nvm
git clone https://github.com/edc/bass.git
cd bass
make install
```

### Paste This into ~/.config/fish/config.fish

```
function nvm
   bass source (brew --prefix nvm)/nvm.sh --no-use ';' nvm $argv
end

set -x NVM_DIR ~/.nvm
nvm use default --silent
```

### Run source

```
source ~/.config/fish/config.fish
```

### You will see this, Don't panic!

```
N/A: version "default -> N/A" is not yet installed.
```

### Don't run this
```
nvm install default
```

### Instead run this
```
nvm install x.x.x
```

### Useful command
```
nvm ls-remote
nvm ls
nvm use default
nvm use x.x.x
nvm alias default 'lts/*'
```
