# TypeScript Node Base Application
This is a template to create TypeScript Node applications. The following template includes:
- `package.json` file minimally configured
- `concurrently` npm package allows us to execute concurrent npm scripts independent from the OS
that we are working on
- Easy start using `nodemon`
- Linting preconfigured
- Node type definition files pre installed
- `git` minimally configured through a `.gitignore` file
- TypeScript minimally configured through `tsconfig.json`

## Prerequisites
Node and NPM must be installed in your system before using this template. The recommended way to
install Node in your system is using a Node version manager:
- Linux: [nvm](https://nvm.sh)
- Windows: [nvs](https://github.com/jasongin/nvs)

## package.json file
It was created like this:
```sh
$ npm init -y

```

### Scripts
TBD

## .tsconfig.json file
### Creation
It was created using TypeScript NPM package as a global installation:
```sh
$ npm install -g typescript

$ tsc init -y

```

### Configuration
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

## Node type definitions
They are necessary to use Node APIs (like `crypto` or `fs`) in your TypeScript code. They were
installed like this:
```sh
$ npm install -D @types/node

```

## Concurrently
`concurrently` has been installed like this:
```sh
$ npm install -D concurrently

```

## Nodemon
`nodemon` was installed like this:
```sh
$ npm install -D nodemon

```

## How to use this template for your projects?
Just clone this repository and specify the name of your project:
```sh
$ git clone https://github.com/andresmunozit/ts-node-base-application.git name-of-your-project

```
