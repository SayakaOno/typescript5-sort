## tsconfig.json

- generate tsconfig.json

```
tsc --init
```

- settings in tsconfig.json

```
"outDir": "./build",
"rootDir": "./src"
```

- run

```
tsc -w
```

## run multiple scripts(concurrently) and execute(nodemon) automatically

- install packages

```
npm install nodemon concurrently
```

- settings in package.json

```
"scripts": {
  "start:build": "tsc -w",
  "start:run": "nodemon build/index.js",
  "start": "concurrently npm:start:*"
}
```
