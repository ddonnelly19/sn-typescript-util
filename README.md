# SN TypeScript Util

A [TypeScript](https://www.typescriptlang.org/) CLI utility that works on-top of the ServiceNow Extension for VS Code. This tool activates a TypeScript-based workflow for ServiceNow developers using VS Code.

## Benefits

Using TypeScript, the CLI provides an enhanced developer workflow.

- Work in modern JavaScript ES2015 (ES6) and beyond
- Extend JavaScript by using types
- Unlock code navigation and intelligent code completion
- Catch bugs before syncing to the instance

## Prerequisites

- [Node.js](https://nodejs.org/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [ServiceNow Extension for VS Code](https://marketplace.visualstudio.com/items?itemName=ServiceNow.now-vscode)
- A [project created](https://docs.servicenow.com/bundle/quebec-application-development/page/build/applications/task/create-project.html#create-project) and [application imported](https://docs.servicenow.com/bundle/quebec-application-development/page/build/applications/task/create-project.html#vscode-import-application) in VS Code

## Installation & Setup

Install the npm package.

```bash
npm install -g sn-typescript-util
```

Build the TypeScript and configuration files. This only needs to be done once for an application.

```bash
snts --build
```

In the application directory created by the ServiceNow Extension, the build creates a `ts` directory from the JavaScript files in the `src` directory. This is where all the TypeScript code resides and where the workflow begins.

## Basic Workflow

After installation & setup, use the watch command to start looking for TypeScript code changes in the `ts` directory.

```bash
snts --watch
```

Or simply invoke `nodemon`. This will watch for changes and provide verbose logging as they occur.

```bash
nodemon
```

Any JavaScript ES2015 (ES6) code added will get converted down to ES5 and moved to the `src` directory. Then changes are ready to sync with the target instance using the ServiceNow Extension for VS Code.

## License

[MIT License](LICENSE)
