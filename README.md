# TypeScript Node Base Application

## What does this repository include?
- A `package.json` file minimally configured
- A `dev` script using [ts-node-dev](https://www.npmjs.com/package/ts-node-dev)
- A `release` script for automatic `CHANGELOG.md` generation using
[standard-version](https://www.npmjs.com/package/standard-version)
- A `.gitignore` file
- Node type definitions `@types/node` installed
- TypeScript minimally configured through `tsconfig.json`

## What it will include in the future?
- Linting

## Prerequisites
- Linux and Mac: [nvm](https://nvm.sh)
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

## CHANGELOG.md Automatic Generation
[standard-version](https://www.npmjs.com/package/standard-version) package is being used for
generating the CHANGELOG.md file. You must follow
[conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) specification in your
commits.

The `standard-version` package is installed as a dev dependency. This is how you can use it:
```sh
# It will update the package.json version, generate the CHANGELOG.md file, tag based on the latest
# package.json version and commit those changes
$ npm run release -- [standard-version options]

# Example
$ npm run release -- --first-release

> ts-node-base-application@0.0.1 release
> standard-version "--first-release"

✖ skip version bump on first release
✔ created CHANGELOG.md
✔ outputting changes to CHANGELOG.md
✔ committing CHANGELOG.md
✔ tagging release v0.0.1
ℹ Run `git push --follow-tags origin main` to publish

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
