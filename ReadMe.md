2.3 Les erreurs sont :

- Indentation
- Manque de points-virgules
- Usage de console.log (règle no-console activée)
- Espacement autour des opérateurs (space-infix-ops) : const x=10; devrait être const x = 10;

3.2

npx husky add .husky/pre-commit "npx eslint ."
husky - add command is DEPRECATED

Du coup j'ai fais : mkdir -p .husky
touch .husky/pre-commit
chmod +x .husky/pre-commit

''''
echo '#!/bin/sh
. "$(dirname "$0")/_/husky.sh"

npx eslint .' > .husky/pre-commit
''''


3.3 

''''
git commit -m "Test du hook ESLint"
husky - DEPRECATED

Please remove the following two lines from .husky/pre-commit:

#!/usr/bin/env sh
. "$(dirname -- "$0")/_/husky.sh"

They WILL FAIL in v10.0.0

[main (root-commit) 954e502] Test du hook ESLint
 7 files changed, 1097 insertions(+)
 create mode 100644 .gitignore
 create mode 100755 .husky/pre-commit
 create mode 100644 ReadMe.md
 create mode 100644 app.js
 create mode 100644 eslint.config.mjs
 create mode 100644 package-lock.json
 create mode 100644 package.json
''''


