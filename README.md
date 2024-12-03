step 1: 
``` bash
npm init -y
```
-y is for yes to all the questions
step 2: 
``` bash
npm install typescript @types/node
```
step 3: 
``` bash
npm install -D <your other packages like express>

```
-D is for dev dependencies,this is for the packages that are only used in development

```bash
npm install dotenv
```
dotenv is for the environment variables, it is used to store the environment variables in the .env file

```
touch tsconfig.json
```
tsconfig.json is for the typescript configuration, it is used to configure the typescript compiler


in tsconfig.json, we need to add the following:
```json
{
    "compilerOptions": {
        "outDir": "./dist",
        "rootDir": "./src",
        "target": "ES2022",
        "module": "NodeNext",
        "moduleResolution": "NodeNext",
        "strict": true,
        "esModuleInterop": true,
        "skipLibCheck": true,
        
    },
    "include": ["src/**/*.ts"],
    "exclude": ["node_modules"]
}
```
outDir is for the output directory, it is the directory where the compiled code will be stored
rootDir is for the root directory, it is the directory where the source code is stored
target is for the target version of javascript, it is the version of javascript that the code will be compiled to
module is for the module system, it is the module system that the code will be compiled to
moduleResolution is for the module resolution, it is the module resolution that the code will be compiled to
strict is for the strict mode, it is the strict mode that the code will be compiled to
esModuleInterop is for the esmodule interoperability, it is the esmodule interoperability that the code will be compiled to
skipLibCheck is for the skip library check, it is the skip library check that the code will be compiled to

```bash
touch .gitignore
```
.gitignore is for the git ignore, it is the git ignore that the code will be compiled to

in .gitignore, we need to add the following:
```
node_modules
dist
.env
.env.*
```

in package.json, we need to change the following:
```json
"scripts": {
    "build": "tsc",
    "start": "tsc && node dist/index.js"
}
```

```bash
mkdir src
```
src is for the source code, it is the directory where the source code is stored


```bash
touch src/index.ts
```
index.ts is for the entry point of the application, it is the file that will be executed when the application is run

in index.ts test out that building and starting the application works

```typescript
async function main(){
    console.log("Hello World");
}

main();
```

then in terminal run:

```bash
npm run start
```
