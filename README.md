# TypeScript Node Base Application
This is a template to create TypeScript Node applications. The following template includes:
- `package.json` file minimally configured
- An easy start script in dev mode using [ts-node-dev](https://www.npmjs.com/package/ts-node-dev)
- Node type definition files pre installed
- `.gitignore` file
- TypeScript minimally configured through `tsconfig.json`
- Linting preconfigured - TODO

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

> ts-node-base-application@1.0.0 start
> ts-node-dev --respawn src/index.ts

[INFO] 14:26:13 ts-node-dev ver. 1.1.8 (using ts-node ver. 9.1.1, typescript ver. 4.6.4)
Application was executed...

# Start editing the src/index.ts file :)

```

## How this template was configured?

### package.json file
It was created like this:
```sh
$ npm init -y

```

#### Scripts
- TODO

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
