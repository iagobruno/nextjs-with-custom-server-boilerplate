# nextjs-with-custom-server-boilerplate

A boilerplate of an [Express](https://www.npmjs.com/package/express) server that renders pages (made with [React components](https://reactjs.org/docs/components-and-props.html)) using [NextJS](https://github.com/zeit/next.js).

I made this project for future personal use but if you want you can use it too. 👍

## Packages and tools used

- [express](https://www.npmjs.com/package/express)
- [next](https://github.com/zeit/next.js): Render React components in server-side.
- [react](http://reactjs.org)
- [typescript](https://typescriptlang.org): To ensure code type-safety.
- [ts-node-dev](https://www.npmjs.com/package/ts-node-dev): Run Typescript files on Node without manually compiling them before.

## Installation

```
git clone https://github.com/iagobruno/nextjs-with-custom-server-boilerplate.git
cd nextjs-with-custom-server-boilerplate
yarn install
```

## CLI commands

- **`yarn run start:dev`**: Start server in development mode on port 3000 using ts-node-dev. It will restart if you make changes to any file.
  - You can use `--api-only` argument to prevent starting nextjs.
- **`yarn run start:debug`**: Same as the above command but optimized to be attached by [VS Code debugger](https://code.visualstudio.com/docs/editor/debugging).
- **`yarn run build`**: Compile server and client codes into a production optimized version.
- **`yarn run start`**: Start server in production mode. **Requires the "build" command to be executed first!**

## Folder structure

```
.
├── .vscode
├── client  // Contains all client-side codes.
│   ├── components  // Folder with React components.
│   ├── pages  // Folder with Next's Page components.
│   ├── next.config.js  // Self explanatory.
│   └── tsconfig.json  // TypeScript compiler options specific to client codes.
├── common  // Contain files that are used in many parts of the project.
├── dist  // Folder where compiled server code will be placed by the "build" script.
├── public  // Contains static files to be publicly served by Express.
├── server
│   ├── main.ts  // Config express server.
│   ├── next.ts  // Init NextJS.
│   └── start.ts  // Start express server.
├── globals.d.ts
├── tsconfig.json  // Main Typescript compiler options
├── package.json
└── yarn.lock
```
