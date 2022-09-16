# Practice of npm/yarn package managers

## NPM

> **Note:** Always use: npm help

1. Project initialization

- npm init (to init the project)
- npm init --yes (to momentally init the project)

2. Package searching

- npm search <`package-name`>
- npm view <`package-name`> (to see more detailed info)
- npm repo <`package-name`> (to open the package repo on github)
- npm home <`package-name`> (to see the homepage of the package)
- npm s "bootstrap grid" (to search with many words)

3. Package installation

- npm install <`package-name`>
- npm install <`package-name`>@4.1.1 (to install specific version of the package)
- npm i <`package-name`> --save-prod (add package to dependencies)
- npm i <`package-name`> --save-dev (add package to devDependencies)
- npm i <`package-name`> --global (to install package globally to your OS, recommended only to exec. files)
- npm list --depth=0 (to see installed packages with certain depth level)
- npm list -g (to see the global packages)
- npm root -g (to see where are the global packages)

4. Types of dependencies

> **Note:** There are 2 main types: dependencies & devDependencies

Dependencies: needed in production(react, normalize, etc...) 
DevDependencies: needed only during the work (bundlers, linters, test tools, etc...)

5. Execution files & NPM scripts, configs

You can make new script instructions in package.json file and then:

- npm run <`script-name`> (to run the script)
- npm config <`options`> (to make something as a default, author-name, license, etc...)

6. Package versions

- npm outdated (to see if updates are available to your packages)
- npm remove <`package-name`> (to delete the package)
- npm update <`package-name`> (to update certain package, only to latest minor version)

> **Note:** If you want to change the options of package updating, you need to go to the 
package.json file and look for your package:

"`package-name`": "~version" - patch ver. upd.
"`package-name`": "^version" - minor ver. upd.
"`package-name`": "*" - major ver. upd.

7. NPM on production

- .gitignore -> node_modules
- npm i (to install all required packages, with info from package-lock.json file where all is logged)
- npm i --production (installing without devDependencies)
- npm ci (install packages from package-lock.json file, with exact versions)

## Yarn

> **Note:** Always use: yarn help
Yarn is similar to the NPM

1. Project initialization

- yarn init
- yarn config <`config-name`> (to change some default params)

2. Package installation/changing

- yarn add <`package-name`>
- yarn add <`package-name`>@<`version`> (add specif. version)
- yarn add <`package-name`> --dev (add to devDependencies)
- yarn global add <`package-name`>
- yarn install (to install everything from package.json)
- yarn remove <`package-name`> 
- yarn upgrade <`package-name`>
- yarn outdated (if have upds)

3. Running scripts

- yarn <`script-name`>

4. Additional things

- yarn check (see if packages are the latest ver.)
- yarn import (creates a new yarn file from existing node_modules folder)
- yarn autoclean --init (to init the autoclean file)
- yarn autoclean --force (to force clean node_modules from useless dependecies)
- yarn global bin (directory, where global modules are saved)
- yarn pack (to pack your project)