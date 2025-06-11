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


