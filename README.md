# TypeScript Node Base Application
This is a template to create TypeScript Node applications. The following template includes:
- `package.json` file minimally configured
- An easy start script in dev mode using `nodemon`
- `concurrently` npm package allows us to execute concurrent npm scripts independent from the OS
that we are working on
- Linting preconfigured
- Node type definition files pre installed
- `git` minimally configured through a `.gitignore` file
- TypeScript minimally configured through `tsconfig.json`

## Prerequisites
Node and NPM must be installed in your system before using this template. The recommended way to
install Node in your system is using a Node version manager:
- Linux: [nvm](https://nvm.sh)
- Windows: [nvs](https://github.com/jasongin/nvs)

## How to use this template for your projects?
Follow the next steps:
```sh
# Clone this repository and specify the name of your project:
$ git clone https://github.com/andresmunozit/ts-node-base-application.git name-of-your-project

# Get into your project's directory
$ cd name-of-your-project

# Install TypeScript globally
$ npm install -g typescript

# Install the dependencies
$ npm install

# Run the start script (the first time is going to crash, exit using Control + C and run it again)
$ npm start
11:33:25 - Starting compilation in watch mode...
[start:build]
[start:run] [nodemon] 2.0.13
[start:run] [nodemon] to restart at any time, enter `rs`
[start:run] [nodemon] watching path(s): *.*
[start:run] [nodemon] watching extensions: js,mjs,json  
[start:run] [nodemon] starting `node build/index.js`    
[start:run] Application has started!
[start:run] [nodemon] clean exit - waiting for changes before restart

# Start editing the src/index.ts file :)

```

## How this template was configured?

### package.json file
It was created like this:
```sh
$ npm init -y

```

#### Scripts
- `"start:build": "tsc -w"` - Compiles all the TypeScript files in `/src/*` to JavaScript in
`/build/*` and stay in watch mode (recompiles if any change takes place inside of `/src/*`) 
- `"start:run": "nodemon build/index.js"` - Starts the JavaScript compiled application using
nodemon, any change on `/build/*` will restart the application
- `"start": "concurrently npm:start:*"` - Runs `start:build` and then `start:run`

### .tsconfig.json file
#### Creation
It was created using TypeScript NPM package as a global installation:
```sh
$ npm install -g typescript

$ tsc init -y

```

#### Configuration
The only modifications to this file are being listed bellow:
```json
// tsconfig..json
{
  "compilerOptions": {
    // ...
    // "rootDir" has been uncommented and set to "./src"
    "rootDir": "./src",   /* Specify the root folder within your source files. */
    // ...
    // "outDir" has been uncommented and set to "./build"
    "outDir": "./build",  /* Specify an output folder for all emitted files. */
    // ...
  }
}

```

### Node type definitions
They are necessary to use Node APIs (like `crypto` or `fs`) in your TypeScript code. They were
installed like this:
```sh
$ npm install -D @types/node

```

### Concurrently
`concurrently` has been installed like this:
```sh
$ npm install -D concurrently

```

### Nodemon
`nodemon` was installed like this:
```sh
$ npm install -D nodemon

```

### test-marsal-1
