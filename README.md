# React Native Template Boilerplate

This is the boilerplate project that includes navigation and other essential setups. Use this template to kickstart your React Native project without worrying about initial configurations. Please refer to the README file for setup instructions and a detailed explanation of the boilerplate structure.

## Usage

```bash
npx @react-native-community/cli@latest init "YourProjectName" --template @ankitmistry/rn-boilerplate-template
```

## Features

- **Folder Structure:** Organized folder layout for API, Redux, assets, components, screens, and more.
- **Redux Integration:** Includes Redux setup with slices for managing loader and profile states.
- **Asset Management:** Handles fonts and images with an export setup for easy access.
- **Internationalization (i18n):** Localization support with English language translations.
- **Navigation:** Configured with React Navigation for stack and bottom tab navigation.
- **Utility Functions:** Common utilities like async services and constants provided.
- **Custom Components:** Reusable UI components like loaders and styled text components.
- **TypeScript Support:** Includes TypeScript type definitions for enhanced development.

## Project Folder Structure

```
📁src
│
├── 📁api
│   ├── APIManager.ts
│   └── index.ts
│
├── 📁appredux
│   ├── 📁Modules
│   │   ├── LoaderSlice.ts
│   │   ├── ProfileSlice.ts
│   │   └── index.ts
│   └── index.ts
│
├── 📁assets
│   ├── 📁Fonts
│   │   ├── Inter-Black.ttf
│   │   ├── Inter-Bold.ttf
│   └── 📁Images
│       ├── IC_Close.svg
│       ├── IC_CloseWhite.svg
│       └── index.ts
│
├── 📁common
│   ├── asyncServices.ts
│   ├── constant.ts
│   └── index.ts
│
├── 📁components
│   ├── CustomLoader.tsx
│   ├── PrimaryText.tsx
│   └── index.ts
│
├── 📁data
│   └── index.ts
│
├── 📁hooks
│   └── index.ts
│
├── 📁i18n
│   ├── en.ts
│   └── index.ts
│
├── index.tsx
│
├── 📁navigation
│   ├── MainNavigation.tsx
│   ├── RootNavigation.tsx
│   └── index.ts
│
├── 📁screens
│   ├── 📁Home
│   │   └── index.tsx
│   ├── 📁Login
│   │   └── index.tsx
│   └── index.ts
│
├── 📁services
│   └── index.ts
│
├── 📁theme
│   └── index.ts
│
└── 📁types
    └── index.ts
```

## Folder Overview

This section provides a structured overview of the project's folder organization within the `src` directory. Each folder serves a specific purpose and contains relevant files necessary for developing and maintaining the React Native application. Importing and exporting within the project is centralized through the `index.ts` files located in each parent folder.

### api

Contains API-related files.

- `APIManager.ts`: Manages API calls.
- `index.ts`: Entry point for API-related exports.

### appredux

Contains Redux-related files.

- `LoaderSlice.ts`: Redux slice for loader management.
- `ProfileSlice.ts`: Redux slice for profile management.
- `index.ts`: Entry point for Redux setup.

### assets

Contains fonts and images used in the application.

- **Fonts:** Inter-Black.ttf, Inter-Bold.ttf, and more.
- **Images:** IC_Close.svg, IC_CloseWhite.svg
- `index.ts`: Exports image resources.

### common

Contains common utility functions and constants.

- `asyncServices.ts`: Handles asynchronous services.
- `constant.ts`: Contains application constants.
- `index.ts`: Entry point for common utility exports.

### components

Contains reusable UI components.

- `CustomLoader.tsx`: Custom loader component.
- `PrimaryText.tsx`: Component for primary text styling.
- `index.ts`: Entry point for component exports.

### data

Contains data-related configurations.

- `index.ts`: Entry point for data configurations.

### hooks

Contains custom React hooks.

- `index.ts`: Entry point for custom hook exports.

### i18n

Contains internationalization files.

- `en.ts`: English language translations.
- `index.ts`: Entry point for internationalization exports.

### navigation

Contains navigation-related components.

- `MainNavigation.tsx`: Main navigation configuration.
- `RootNavigation.tsx`: Root navigation setup.
- `index.ts`: Entry point for navigation exports.

### screens

Contains screen components for the application.

- **Home:** `index.tsx` — Home screen component.
- **Login:** `index.tsx` — Login screen component.
- `index.ts`: Entry point for exporting screen components.

### services

Contains service layer configurations.

- `index.ts`: Entry point for service configurations.

### theme

Contains theme-related configurations.

- `index.ts`: Entry point for theme configurations.

### types

Contains TypeScript type definitions.

- `index.ts`: Entry point for type definitions.

## Babel Aliases

The project uses Babel aliases to simplify imports. By default, the following aliases are configured:

| Alias         | Path               |
| ------------- | ------------------ |
| `@api`        | `./src/api`        |
| `@appredux`   | `./src/appredux`   |
| `@assets`     | `./src/assets`     |
| `@common`     | `./src/common`     |
| `@components` | `./src/components` |
| `@data`       | `./src/data`       |
| `@hooks`      | `./src/hooks`      |
| `@i18n`       | `./src/i18n`       |
| `@navigation` | `./src/navigation` |
| `@screens`    | `./src/screens`    |
| `@services`   | `./src/services`   |
| `@theme`      | `./src/theme`      |
| `@apptypes`   | `./src/types`      |

## Customizing or Adding Aliases

To create custom aliases or add additional folders:

1. **Create a New Folder:** Inside the `src` directory, create a new folder for your module or functionality.

2. **Index File:** Inside your new folder, create an `index.ts` file. Import all files and modules from this folder and export them.

3. **Modify Babel Configuration:** Update `babel.config.js`:

```js
module.exports = {
  plugins: [
    [
      "module-resolver",
      {
        alias: {
          "@newAlias": "./src/newFolder",
        },
      },
    ],
  ],
};
```

4. **Update TypeScript Configuration:** Modify `tsconfig.json`:

```json
{
  "compilerOptions": {
    "baseUrl": "./",
    "paths": {
      "@newAlias/*": ["src/newFolder/*"]
    }
  }
}
```

## How to Start the Project

Install node_modules:

```bash
npm install
```

Run on Android:

```bash
npm run android
```

Run on iOS:

```bash
npm run ios
```

Start Metro bundler:

```bash
npm start
```

---

Powered by [React Native](https://reactnative.dev)
