# cli-app-nodejs

The guide I am following: https://developer.okta.com/blog/2019/06/18/command-line-app-with-nodejs

run ``npm ini``t -> This really just created the package.json, couldn't see any other output.
commit 

Run ``node .`` while in the cli-app-nodejs dir to run the package.

**install a local developed app in your global system**

Create a project structure like so:
- cli-app-nodejs
    - index.js
    - package.json

-- index.js --
```
#!/usr/bin/env node

console.log("Hello World GW")
```

-- package.json --
```
{
  "name": "cli-app-nodejs",
  "bin": {
    "cli-app-nodejs": "index.js"
  }
}
```

Navigate to the cli-app-nodejs dir on the command line and run `npm link` - this will install the package globally.

Run ``cli-app-nodejs`` as a command to run the package and print 'Hello World GW'!

run ``npm ls -g`` to check which packages are installed and usable globally. After running npm link, the cli-app-nodejs packages should be here.

run ``npm remove -f <package-name>`` to remove on of those package. E.g. ``npm remove -g my_module``
