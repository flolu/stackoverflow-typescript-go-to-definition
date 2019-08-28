# Setup

```
yarn bootstrap
```

# Gist

All source code file are written in Typescript (`.ts`) under `/src` folder.

All compiled files (`.js` and `.ts`) are located under `/dist` (those files are created by the typescript compiler)

# Replicate Issue

> This issue happens in Visual Studio Code

1. Run `yarn bootstrap`
2. Open `/services/example-service/src/index.ts`
3. Right click on `Food` and choose "Go to Definition"

## Current behavior

VSCode opens `/packages/example-package/dist/index.d.ts`

## Expected behavior

VSCode opens `/packages/example-package/src/index.ts`

# Issue

When I'm editing the typescript source code (in `/src`), I want to be able to click on any imported object via `right click + go to definition` or `F12` to jump to the definition in the respective packages' `/src` folder.

But what happens instead, is that it opens the `.d.ts` file in the `/dist` folder.

> Is it possible to change this behavior?
