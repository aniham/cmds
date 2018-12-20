##### brew

list available node versions

```
brew search node
```

install specific version (less granular than nvm, installs latest stable minor version)

```
brew install node@10
```

use specific version

```
brew unlink node
brew link node@10
```

##### nvm

list available node versions

```
nvm ls
```

install specific version

```
nvm install 10.14.2
```

use specific version

```
nvm use 10.14.2
```
