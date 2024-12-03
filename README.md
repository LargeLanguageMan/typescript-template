# TypeScript Node.js Project Setup Guide

This guide will help you set up a Node.js project with TypeScript.

## Initial Setup

1. Initialize a new Node.js project
```bash
npm init -y
```

2. Install TypeScript and Node.js types
```bash
npm install typescript @types/node
```

3. Install development dependencies (if needed)
```bash
npm install -D <your-dev-dependencies>  # e.g., express, jest, etc.
```

4. Install environment variables support
```bash
npm install dotenv
```

## Configuration Files

### TypeScript Configuration
Create a `tsconfig.json` file:
```bash
touch tsconfig.json
```

Add the following configuration:
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
        "skipLibCheck": true
    },
    "include": ["src/**/*.ts"],
    "exclude": ["node_modules"]
}
```

### Git Configuration
Create a `.gitignore` file:
```bash
touch .gitignore
```

Add the following entries:
```
node_modules
dist
.env
.env.*
```

### Package.json Scripts
Update your `package.json` with these scripts:
```json
{
    "scripts": {
        "build": "tsc",
        "start": "tsc && node dist/index.js"
    }
}
```

## Project Structure

1. Create source directory:
```bash
mkdir src
```

2. Create entry point file:
```bash
touch src/index.ts
```

## Test Your Setup

1. Add this code to `src/index.ts`:
```typescript
async function main() {
    console.log("Hello World");
}

main();
```

2. Run the project:
```bash
npm run start
```

## Configuration Details

- **outDir**: Compiled JavaScript output directory
- **rootDir**: TypeScript source code directory
- **target**: JavaScript version for compilation (ES2022)
- **module**: Module system (NodeNext)
- **moduleResolution**: Module resolution strategy
- **strict**: Enable strict type checking
- **esModuleInterop**: Enable ES Module interop
- **skipLibCheck**: Skip type checking of declaration files

## Next Steps

1. Start adding your source code in the `src` directory
2. Create a `.env` file for environment variables
3. Install additional dependencies as needed
4. Begin building your application!
