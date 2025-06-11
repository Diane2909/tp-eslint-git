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

5.3 
dans Action : 1 workflow run
''''
Ajout de GitHub Actions
.github/workflows/lint.yml #1: Commit 500baa6 pushed by Diane2909
''''


Pour le fichier discord :
npx eslint .                                                        


/Users/dianerobilliard/tp-eslint-git/app.js
  2:1  warning  Unexpected console statement  no-console
  5:3  warning  Unexpected console statement  no-console

/Users/dianerobilliard/tp-eslint-git/app2.js
   1:23  error    A space is required after ','                                                                          comma-spacing
   1:26  error    Missing space before opening brace                                                                     space-before-blocks
   2:1   error    Expected indentation of 2 spaces but found 4                                                           indent
   2:9   error    'result' is never reassigned. Use 'const' instead                                                      prefer-const
   2:15  error    Operator '=' must be spaced                                                                            space-infix-ops
   2:17  error    Operator '+' must be spaced                                                                            space-infix-ops
   2:19  error    Missing semicolon                                                                                      semi
   3:1   error    Expected indentation of 2 spaces but found 4                                                           indent
   3:5   warning  Unexpected console statement                                                                           no-console
   3:34  error    A space is required after ','                                                                          comma-spacing
   3:42  error    Missing semicolon                                                                                      semi
   4:1   error    Expected indentation of 2 spaces but found 4                                                           indent
   4:18  error    Missing semicolon                                                                                      semi
   5:1   error    Expected indentation of 0 spaces but found 4                                                           indent
   6:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
   7:1   error    Expected indentation of 0 spaces but found 4                                                           indent
   7:11  error    'unusedVar' is assigned a value but never used                                                         no-unused-vars
   8:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
   9:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  10:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  10:13  error    Expected '===' and instead saw '=='                                                                    eqeqeq
  11:1   error    Expected indentation of 4 spaces but found 8                                                           indent
  11:9   warning  Unexpected console statement                                                                           no-console
  11:21  error    Strings must use singlequote                                                                           quotes
  11:43  error    Missing semicolon                                                                                      semi
  12:1   error    Expected indentation of 4 spaces but found 8                                                           indent
  12:15  error    Missing semicolon                                                                                      semi
  13:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  14:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  14:7   error    Function 'division' expected no return value                                                           consistent-return
  14:19  error    Missing semicolon                                                                                      semi
  15:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  16:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
  17:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  17:5   warning  Unexpected console statement                                                                           no-console
  17:30  error    A space is required after ','                                                                          comma-spacing
  18:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
  19:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  19:11  error    'message' is assigned a value but never used                                                           no-unused-vars
  19:39  error    Missing semicolon                                                                                      semi
  20:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
  21:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  21:9   warning  Unexpected constant condition                                                                          no-constant-condition
  22:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  22:7   warning  Unexpected console statement                                                                           no-console
  22:19  error    Strings must use singlequote                                                                           quotes
  22:51  error    Missing semicolon                                                                                      semi
  23:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  24:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
  25:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  25:11  error    'tableau' is assigned a value but never used                                                           no-unused-vars
  26:1   error    Expected indentation of 2 spaces but found 4                                                           indent
  27:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  28:1   error    Expected indentation of 2 spaces but found 4                                                           indent
  28:13  error    Missing trailing comma                                                                                 comma-dangle
  29:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  29:6   error    Missing semicolon                                                                                      semi
  30:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
  31:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  31:24  error    Missing semicolon                                                                                      semi
  32:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  32:16  error    Expected '===' and instead saw '=='                                                                    eqeqeq
  33:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  33:7   warning  Unexpected console statement                                                                           no-console
  33:38  error    Missing semicolon                                                                                      semi
  34:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  35:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
  36:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  36:14  error    'toutFaire' is defined but never used                                                                  no-unused-vars
  37:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  37:7   warning  Unexpected console statement                                                                           no-console
  37:27  error    Missing semicolon                                                                                      semi
  38:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  38:18  error    Missing semicolon                                                                                      semi
  39:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  39:18  error    Missing semicolon                                                                                      semi
  40:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  40:18  error    Missing semicolon                                                                                      semi
  41:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  41:18  error    Missing semicolon                                                                                      semi
  42:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  42:18  error    Missing semicolon                                                                                      semi
  43:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  43:18  error    Missing semicolon                                                                                      semi
  44:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  44:18  error    Missing semicolon                                                                                      semi
  45:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  45:18  error    Missing semicolon                                                                                      semi
  46:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  46:18  error    Missing semicolon                                                                                      semi
  47:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  47:19  error    Missing semicolon                                                                                      semi
  48:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  48:7   warning  Unexpected console statement                                                                           no-console
  48:20  error    A space is required after ','                                                                          comma-spacing
  48:22  error    A space is required after ','                                                                          comma-spacing
  48:24  error    A space is required after ','                                                                          comma-spacing
  48:26  error    A space is required after ','                                                                          comma-spacing
  48:28  error    A space is required after ','                                                                          comma-spacing
  48:30  error    A space is required after ','                                                                          comma-spacing
  48:32  error    A space is required after ','                                                                          comma-spacing
  48:34  error    A space is required after ','                                                                          comma-spacing
  48:36  error    A space is required after ','                                                                          comma-spacing
  48:39  error    Missing semicolon                                                                                      semi
  49:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  49:7   warning  Unexpected console statement                                                                           no-console
  49:25  error    Missing semicolon                                                                                      semi
  50:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  51:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
  52:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  53:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  53:7   warning  Unexpected console statement                                                                           no-console
  53:29  error    Missing semicolon                                                                                      semi
  54:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  54:7   error    Missing semicolon                                                                                      semi
  55:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
  56:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  56:11  error    'd' is assigned a value but never used                                                                 no-unused-vars
  56:25  error    Missing semicolon                                                                                      semi
  57:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
  58:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  58:14  error    'fetchData' is defined but never used                                                                  no-unused-vars
  59:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  60:1   error    Expected indentation of 4 spaces but found 8                                                           indent
  60:15  error    Expected parentheses around arrow function argument                                                    arrow-parens
  60:43  error    Missing semicolon                                                                                      semi
  61:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  62:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
  63:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  63:11  error    'nombres' is assigned a value but never used                                                           no-unused-vars
  63:35  error    Expected parentheses around arrow function argument                                                    arrow-parens
  63:40  error    Unexpected block statement surrounding arrow body; move the returned value immediately after the `=>`  arrow-body-style
  64:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  64:19  error    Missing semicolon                                                                                      semi
  65:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  65:7   error    Missing semicolon                                                                                      semi
  66:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
  67:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  67:5   error    Unexpected 'debugger' statement                                                                        no-debugger
  67:13  error    Missing semicolon                                                                                      semi
  68:1   error    Trailing spaces not allowed                                                                            no-trailing-spaces
  69:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  70:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  70:7   error    Expected property shorthand                                                                            object-shorthand
  71:1   error    Expected indentation of 2 spaces but found 6                                                           indent
  71:15  error    Missing trailing comma                                                                                 comma-dangle
  72:1   error    Expected indentation of 0 spaces but found 4                                                           indent
  72:6   error    Newline required at end of file but not found                                                          eol-last
  72:6   error    Missing semicolon                                                                                      semi

✖ 151 problems (139 errors, 12 warnings)
  128 errors and 0 warnings potentially fixable with the `--fix` option.