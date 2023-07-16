# NodeJs project with TS and Jest

## Steps:

1. create a new directory for the project:

`mkdir node-project-ts`

2. cd in that new directory and open VS code; from now the integrated terminal will be used; initialize the node project

`cd node-project-ts`

`code .`

`npm init -y`

3. install typescript as development dependency

`npm i -D typescript`

4. setup typescript

`npx tsc --init`

5. inside `tsconfig.json`, set the following:

`"rootDir": "./src"`

`"outDir": "./dist"`

6. verify that it works by creating a `src` directory, and in that, `index.ts` file with the code:

`console.log('Hello TS')`

run `npx tsc` command and after that, run `node dist/index.js`

7. install `jest`, the needed types and `ts-jest` in order to easily use it in typescript (as development dependencies)

`npm i -D jest @types/jest ts-jest`

8. setup jest

`npx ts-jest config:init`

9. verify that it works by creating a file `index.test.ts` in the root or in src directory, and add some basic test to check our setup:

```JS
test("test the failing test", () => {
    expect(1).toBe(2)
})
test("test the pass test", () => {
    expect(1).toBe(1)
})

```

`npx jest`

10. make things automated

`npm i -D nodemon`

`npm i -D ts-node`

in `package.json` file, insert the following as `scripts`:

```JSON
 "start": "nodemon --exec ts-node src/index.ts",
  "test": "npx jest"
```

 11. create `.gitignore` file in the root directory of your project and put in that file the following for now:

 ```
 node_modules
 dist
 ```

 `git init`

 Now, the project is configured and ready to add more complexity to it... Happy codding :-)