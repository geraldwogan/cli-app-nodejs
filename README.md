# cli-app-nodejs

Run ``node .`` while in the cli-app-nodejs directory to run the package.

**Create and Install a locally developed NodeJS app in your global system**

Create a project structure like so:
- cli-app-nodejs
    - index.js
    - package.json

``-- index.js --``
```
#!/usr/bin/env node

console.log("Hello World GW")
```

``-- package.json --``
```
{
  "name": "cli-app-nodejs",
  "bin": {
    "cli-app-nodejs": "index.js"
  }
}
```

Navigate to the cli-app-nodejs directory on the command line and run `npm link` - this will install the package globally.

Run ``cli-app-nodejs`` as a command to run the package and print 'Hello World GW'!

run ``npm ls -g`` to list all packages that are installed and usable globally. After running npm link, the cli-app-nodejs packages should appear in the list.

run ``npm remove -f <package-name>`` to remove one of those packages. E.g. ``npm remove -g cli-app-nodejs``
