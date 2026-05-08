## Project Folder Structure

This repository contains the following folder NewProject:

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

This section provides a NewProjectd overview of the project's folder organization within the `src` directory. Each folder serves a specific purpose and contains relevant files necessary for developing and maintaining the React Native application. Importing and exporting within the project is centralized through the `index.ts` files located in each parent folder.

### `api`

Contains API-related files.

- **APIManager.ts**: Manages API calls.
- **index.tsx**: Entry point for API-related exports.

### `appredux`

Contains Redux-related files.

- **LoaderSlice.ts**: Redux slice for loader management.
- **ProfileSlice.ts**: Redux slice for profile management.
- **index.tsx**: Entry point for Redux setup.

### `assets`

Contains fonts and images used in the application.

#### `Fonts`

- **Inter-Black.ttf**
- **Inter-Bold.ttf**

#### `Images`

- **IC_Close.svg**
- **IC_CloseWhite.svg**
- **index.ts**: Exports image resources.

### `common`

Contains common utility functions and constants.

- **asyncServices.ts**: Handles asynchronous services.
- **constant.ts**: Contains application constants.
- **index.ts**: Entry point for common utility exports.

### `components`

Contains reusable UI components.

- **CustomLoader.tsx**: Custom loader component.
- **PrimaryText.tsx**: Component for primary text styling.
- **index.ts**: Entry point for component exports.

### `data`

Contains data-related configurations.

- **index.ts**: Entry point for data configurations.

### `hooks`

Contains custom React hooks.

- **index.ts**: Entry point for custom hook exports.

### `i18n`

Contains internationalization files.

- **en.ts**: English language translations.
- **index.ts**: Entry point for internationalization exports.

### `navigation`

Contains navigation-related components.

- **MainNavigation.tsx**: Main navigation configuration.
- **RootNavigation.tsx**: Root navigation setup.
- **index.ts**: Entry point for navigation exports.

### `screens`

Contains screen components for the application.

#### `Home`

- **index.tsx**: Home screen component.

#### `Login`

- **index.tsx**: Login screen component.

#### `index.ts`

- Entry point for exporting screen components.

### `services`

Contains service layer configurations.

- **index.ts**: Entry point for service configurations.

### `theme`

Contains theme-related configurations.

- **index.ts**: Entry point for theme configurations.

### `types`

Contains TypeScript type definitions.

- **index.ts**: Entry point for type definitions.

---

This NewProjectd overview emphasizes the centralization of imports and exports through `index.ts` files within each parent folder, ensuring a streamlined approach to accessing and utilizing functionality throughout the React Native project.

---

## Babel Aliases

The project uses Babel aliases to simplify imports. By default, the following aliases are configured:

- `@api`: './src/api'
- `@appredux`: './src/appredux'
- `@assets`: './src/assets'
- `@common`: './src/common'
- `@components`: './src/components'
- `@data`: './src/data'
- `@hooks`: './src/hooks'
- `@i18n`: './src/i18n'
- `@navigation`: './src/navigation'
- `@screens`: './src/screens'
- `@services`: './src/services'
- `@theme`: './src/theme'
- `@types`: './src/types'

#### Customizing or Adding Aliases

To create custom aliases or add additional folders:

1. **Create a New Folder**: Inside the `src` directory, create a new folder for your module or functionality.
2. **Index File**: Inside your new folder, create an `index.ts` file. Import all files and modules from this folder in `index.ts` and export them from this file.

3. **Modify Babel Configuration**: Update the `babel.config.js` file to include your new alias. Here's an example of how to add a new alias:

   ```javascript
   module.exports = {
     // Existing Babel configuration
     plugins: [
       [
         "module-resolver",
         {
           alias: {
             // Existing aliases
             "@newAlias": "./src/newFolder", // Replace 'newAlias' and 'newFolder' with your custom alias and folder path
             // Add more aliases as needed
           },
         },
       ],
     ],
   };
   ```

4. **Update TypeScript Configuration**: Modify `tsconfig.json` to include your new alias in the `paths` property under `compilerOptions`:

   ```json
   {
     "compilerOptions": {
       "baseUrl": "./",
       "paths": {
         "@newAlias/*": ["src/newFolder/*"] // Replace 'newAlias' and 'newFolder' with your custom alias and folder path
         // Add more aliases as needed
       }
     }
   }
   ```

**By following these steps, you can create and customize aliases to streamline imports and improve project organization in your React Native application.**

---

## System Configuration

The following table lists the system configuration for the development environment:

| System Component     | Configuration      |
| -------------------- | ------------------ |
| **Operating System** | macOS 14.3.1       |
| **CPU**              | Apple M1 (8 cores) |
| **Memory**           | 8.00 GB            |
| **Shell**            | zsh 5.9            |
| **Node**             | v20.11.1           |
| **Yarn**             | v1.22.19           |
| **npm**              | v10.2.4            |
| **Watchman**         | v2024.05.06.00     |
| **CocoaPods**        | v1.13.0            |
| **Xcode**            | v15.2/15C500b      |
| **Java**             | v17.0.11           |
| **Ruby**             | v2.6.10            |

---

## How to Start the Project

1. Install node_modules:

   ```
   npm install
   ```

2. To run on Android:

   ```
   npm run android
   ```

3. To run on iOS:

   ```
   npm run ios
   ```

4. Start Metro bundler:
   ```
   npm start
   ```

---

<div align="center">
<p align="center">
  <img src="https://reactnative.dev/img/header_logo.svg" alt="React Native">
</p>

<p align="center">
  <b>Powered by React Native</b>
</p>
</div>
