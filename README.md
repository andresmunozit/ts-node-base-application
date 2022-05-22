# TypeScript Node Base Application

## What does this repository include?
- A `package.json` file minimally configured
- An easy dev script [ts-node-dev](https://www.npmjs.com/package/ts-node-dev)
- A `.gitignore` file
- Node type definitions `@types/node` installed
- TypeScript minimally configured through `tsconfig.json`

## What it will include in the future?
- Linting

## Prerequisites
- Linux: [nvm](https://nvm.sh)
- Windows: [nvs](https://github.com/jasongin/nvs)

## How to use this template for your projects?
```sh
# Clone this repository and specify the name of your project:
$ git clone https://github.com/andresmunozit/ts-node-base-application.git name-of-your-project

# Get into your project's directory
$ cd name-of-your-project

# Install TypeScript globally
$ npm install -g typescript

# Install the dependencies
$ npm install

# Run the start script (the first time it's going to crash, exit using Control + C and run it again)
$ npm run dev

> ts-node-base-application@0.0.1 dev
> ts-node-dev --respawn src/index.ts

[INFO] 17:03:32 ts-node-dev ver. 1.1.8 (using ts-node ver. 9.1.1, typescript ver. 4.6.4)
Ready! 🚀

# Start editing the src/index.ts file

```

## How was this template configured?

### package.json
```sh
$ npm init -y

```

### .tsconfig.json file
#### Creation
```sh
$ npm install -g typescript

$ tsc init -y

```

#### Configuration
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
