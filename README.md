# NPM

# How to install from github?
The quickest way is to use github organization hosting the project and repository name.
Following is example to install `express` from github to install `master` branch.
```
npm i exressjs/express
```

# How to install from github tag?
```
npm i exressjs/express#4.14.0
```

# How to install from github branch?
```
npm i exressjs/express#develop
```

# How to install from github commit id?
```
npm i exressjs/express#9375abc335sdf324234ds345325c4534f45454
```

# How to get the details of package which is install?
Following is example for express package
```
npm ls express
```

# How to get the list of packages will be install without even installing it in real?
```
npm i --dry-run
```

# How to get the list of globally installed packages?
```
npm ls -g
```
To only get the list of top level tree
```
npm ls -g --depth=0
```

# How to get the description about installed packages?
```
npm ll -g --depth=0
```

# How to get output in json for parsing?
```
npm ls -g --depth=0 --json
```

# Types of dependencies
1. production dependencies
2. development dependencies
3. optional dependencies

Following are command for these options to install packages into these categories

## Full format
```
1. production
npm install --save express
2. development
npm install --dev express
3. optional
npm install --optional express
```
Note: Full format doesn't work with latest `npm`.
## Shortcut format
```
1. production
npm i -S express
2. development
npm i -D express
3. optional
npm i -O express
```

# Semantic version
NPM uses semantic version for package dependencies. Following is format
```
major.minor.patch
```
Following is example.
```
{
    "express":"1.3.4"
}
```

```
{
    "express":"=1.3.4"
}
```

```
{
    "express":"<1.3.4"
}
```
```
{
    "express":"<=1.3.4"
}
```
```
{
    "express":"1.3.*"
}
```
```
{
    "express":"1.3.x"
}
```
```
{
    "express":"1.3"
}
```
```
{
    "express":"~1.3.4"
}
```
```
{
    "express":"^1.3.*"
}
```

# How to update npm itself?
```
npm i npm -g
```

# How to check if any npm packages are outdated?
```
npm outdated
```

# npm configuration

## How to check list of all the npm configurations?
```
npm config list -l
```
Following is sample output.

```
➜  nodejs-npm npm config list -l
; cli configs
long = true
metrics-registry = "https://registry.npmjs.org/"
scope = ""
user-agent = "npm/5.6.0 node/v9.11.1 darwin x64"

; default values
access = null
allow-same-version = false
also = null
always-auth = false
auth-type = "legacy"
bin-links = true
browser = null
ca = null
cache = "/Users/dilipkumar/.npm"
cache-lock-retries = 10
cache-lock-stale = 60000
cache-lock-wait = 10000
cache-max = null
cache-min = 10
cafile = undefined
cert = null
cidr = null
color = true
commit-hooks = true
depth = null
description = true
dev = false
dry-run = false
editor = "vi"
engine-strict = false
fetch-retries = 2
fetch-retry-factor = 10
fetch-retry-maxtimeout = 60000
fetch-retry-mintimeout = 10000
force = false
git = "git"
git-tag-version = true
global = false
global-style = false
globalconfig = "/usr/local/etc/npmrc"
globalignorefile = "/usr/local/etc/npmignore"
group = 20
ham-it-up = false
heading = "npm"
https-proxy = null
if-present = false
ignore-prepublish = false
ignore-scripts = false
init-author-email = ""
init-author-name = ""
init-author-url = ""
init-license = "ISC"
init-module = "/Users/dilipkumar/.npm-init.js"
init-version = "1.0.0"
json = false
key = null
legacy-bundling = false
link = false
local-address = undefined
loglevel = "notice"
logs-max = 10
; long = false (overridden)
maxsockets = 50
message = "%s"
; metrics-registry = null (overridden)
node-options = null
node-version = "9.11.1"
offline = false
onload-script = null
only = null
optional = true
otp = 0
package-lock = true
package-lock-only = false
parseable = false
prefer-offline = false
prefer-online = false
prefix = "/usr/local"
production = false
progress = true
proxy = null
read-only = false
rebuild-bundle = true
registry = "https://registry.npmjs.org/"
rollback = true
save = true
save-bundle = false
save-dev = false
save-exact = false
save-optional = false
save-prefix = "^"
save-prod = false
scope = ""
script-shell = null
scripts-prepend-node-path = "warn-only"
searchexclude = null
searchlimit = 20
searchopts = ""
searchstaleness = 900
send-metrics = false
shell = "/bin/zsh"
shrinkwrap = true
sign-git-tag = false
sso-poll-frequency = 500
sso-type = "oauth"
strict-ssl = true
tag = "latest"
tag-version-prefix = "v"
timing = false
tmp = "/var/folders/8d/ndyvdtrn4tqdd4ynfb4cjbq80000gn/T"
umask = 18
unicode = true
unsafe-perm = true
usage = false
user = 0
; user-agent = "npm/{npm-version} node/{node-version} {platform} {arch}" (overridden)
userconfig = "/Users/dilipkumar/.npmrc"
version = false
versions = false
viewer = "man"

```

## Set default author name for `npm init`
```
npm config set init-author-name "Dilip Kumar"
```
To delete it.
```
npm config delete init-author-name
```

## Set default as save option on npm install
```
npm config set save true
```

# Search npm registry

Sample command to search.
```
npm search lodash
```
Following is sample output.
```
NAME                      | DESCRIPTION          | AUTHOR          | DATE       | VERSION  | KEYWORDS
lodash                    | Lodash modular…      | =jdalton…       | 2018-09-12 | 4.17.11  | modules stdlib util
lodash.debounce           | The lodash method…   | =jdalton…       | 2016-08-13 | 4.0.8    | lodash-modularized debounce
lodash.clonedeep          | The lodash method…   | =jdalton…       | 2016-08-13 | 4.5.0    | lodash-modularized clonedeep
lodash.assign             | The lodash method…   | =jdalton…       | 2016-08-13 | 4.2.0    | lodash-modularized assign
lodash.merge              | The Lodash method…   | =jdalton…       | 2018-02-04 | 4.6.1    | lodash-modularized merge
lodash-es                 | Lodash exported as…  | =jdalton…       | 2018-09-12 | 4.17.11  | es6 modules stdlib util
lodash.template           | The lodash method…   | =jdalton…       | 2016-08-13 | 4.4.0    | lodash-modularized template
lodash.uniq               | The lodash method…   | =jdalton…       | 2016-08-13 | 4.5.0    | lodash-modularized uniq
lodash.isplainobject      | The lodash method…   | =jdalton…       | 2016-08-13 | 4.0.6    | lodash-modularized isplainobject

```

# How to lock npm version?
```
npm shrinkwrap
```
# How to open home page of package
```
npm home lodash
```

# How to open repository of package
```
npm repo lodash
```

# How to clean node_modules for undocumented dependencies?
```
npm prune
```

# How to list all the modules?
```
npm ls
```

# Draw visuals
## Draw face
```
npm visnup
```

## Draw XMAS tree
```
npm xmas
```
