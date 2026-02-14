npm init -y
tsc --init


npm install -D typescript
npm run build
npm pack

npm login
npm publish --access public


*******************************************************
npm version patch
git push --follow-tags
*******************************************************


how to reuse?
npm install @vincentgwzhang/string-utils

```ts
import { capitalize } from "@vincentgwzhang/string-utils";
console.log(capitalize("vincent"));
```




```json
{
  "name": "@vincentgwzhang/string-utils",
  "version": "1.0.0",
  "description": "Simple string utility functions",
  "author": "Vincent Zhang",
  "license": "MIT",

  "main": "dist/index.js",           
  "module": "dist/index.js",         
  "types": "dist/index.d.ts",        

  "exports": {
    ".": {
      "import": "./dist/index.js",
      "require": "./dist/index.js"
    }
  },

  "files": [
    "dist"
  ],

  "scripts": {
    "build": "tsc",
    "prepare": "npm run build"
  },

  "devDependencies": {
    "typescript": "^5.0.0"
  }
}
```