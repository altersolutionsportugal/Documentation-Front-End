# Husky

## Install Husky
[Follow this NPM documentation](https://www.npmjs.com/package/husky)

[Follow this official documentation](https://typicode.github.io/husky/#/)

### Pre-commit
Here we add scripts that will be running on the pre-commit

```shell
#!/bin/sh
. "$(dirname "$0")/_/husky.sh"

yarn test:ci
yarn lint
```
