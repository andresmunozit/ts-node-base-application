# TypeScript Node Base Application
This is a template to create TypeScript Node applications. The following template includes:
- `package.json` file minimally configured
- `concurrently` npm package allows us to execute concurrent npm scripts independent from the OS that
we are working on
- Ready and easy start using Nodemon
- Linting preconfigured
- Node type definition files pre installed
- Git configured
- TypeScript preconfigured with default settings through `tsconfig.json` file

## package.json file
It was created like this:
```sh
$ npm init -y

```

### Scripts


## .tsconfig.json file
### Creation
It was created using TypeScript NPM package as a global insallation:
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


## Node type definition files
It was installed like this:
```sh
$ npm install @types/node

```

## Concurrrently
Concurrently has been installed like this:
```sh
$ npm install concurrently

```