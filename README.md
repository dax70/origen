# Hello Origen

Notes about the steps to set up a development project manually.

### Common Steps
1. Create project directory

  Ex: `> mkdir -p ~/code/proj-name`

* Initialize Git `> git init`
* Add a README.md `> echo 'Readme title' > README.md`
* Add a GitIgnore

  Using [gitignore.io](http://gitignore.io)
For MacOS/Linux

  `curl -o .gitignore https://www.gitignore.io/api/MY_API_NAME`

  Example for macOS and Node:

  `curl -o .gitignore https://www.gitignore.io/api/macos%2Cnode`
  * Editor Configure

    `touch .editorconfig`

## Javascript/Node Development

### Set up NPM
1. Initialize NPM `npm init`

### Setting up Babel
1. Yarn add Babel-CLI `> yarn add babel-cli`
2. Add .babelrc `> echo { "presets": [ed2015]} > .babelrc`

  Add Presets
  ```Javascript
    {
      "presets": ["es2015", ...],
      "plugins": [...]
    }
  ```

### Setting up Flow
1. Add Flow plugin to Babel-CLI

  Ex:
  ```Javascript
  {
    "presets": ["es2015", ...],
    "plugins": [
      ...,
      "transform-flow-strip-types"
    ]
  }
  ```
2. Yarn add Flow-bin `> yarn add flow-bin`
3. Add .flowconfig `> touch .flowconfig`

## Testing
### Adding Jest

## Building a Web server
1. Create index.js file at the root of the source
2. Register babel and bootstrap server/app file.
```javascript
require("babel-register");
require('./server.js');
```

## ESLint
### Add ESLint
1. Install ESLint
* Configure rules (Airbnb?)

## Library Development

### Use Lerma for to breakup packages

## Setting up en Editor

### Nuclide Setup

[Setup Nuclide to use Flow and Eslint (Mac)](https://egghead.io/lessons/react-setup-nuclide-to-use-flow-and-eslint-mac)
