## Packages
Packages are self-contained code libraries that we can install and use in our projects.

## Libraries
A "library" is a collection of pre-written code. Libraries can be private, but many are packaged up nicely, branded and made publicly available for other developers to use in their own projects.

## package.json

Virtually all Node.js projects have a file called package.json, which looks similar to this:

```json
{
  "name": "project-name",
  "version": "1.0.0",
  "description": "Short project summary",
  "main": "index.js",
  "scripts": {
    "myscript": "ENV=development node index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "MIT",
  "dependencies": {
    "express": "^4.13.4"
  }
}
```
### Custom Scripts In package.json
The scripts portion allows us to run commands using an alias, for instance:
```
npm run myscript
```
### Dependencies In package.json
The dependencies section of package.json lists the packages that need to be installed for the project to run properly. In the above example it lists a package called express, and the value ^4.13.4 specifies the version.

full documentation of [package.json from npm Docs](https://docs.npmjs.com/cli/v9/configuring-npm/package-json)

