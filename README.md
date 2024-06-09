# MediGuard

### Prerequisites

- Node.js
- npm or yarn 

### Getting Started

To get started with this project, follow these steps:

#### 1. Clone the repository

```bash
git clone https://github.com/Mipol2/MediGuard-Web.git
cd your-repo-name
```

#### 2. Install dependencies

Using npm:

```bash
npm install
```

Or using yarn:

```bash
yarn install
```

#### 3. Start the development server

Using npm:

```bash
npm run dev
```

Or using yarn:

```bash
yarn dev
```

This will start the development server with HMR enabled. You can now view your application in the browser at `http://localhost:3000`.

### ESLint Configuration

This project uses ESLint for code linting. If you are developing a production application, it is recommended to enable type-aware lint rules.

#### Expanding the ESLint configuration

1. Configure the top-level `parserOptions` property like this:

```json
parserOptions: {
  ecmaVersion: 'latest',
  sourceType: 'module',
  project: ['./tsconfig.json', './tsconfig.node.json'],
  tsconfigRootDir: __dirname,
},
```

2. Replace the recommended ESLint plugin:

```bash
# From
plugin:@typescript-eslint/recommended

# To
plugin:@typescript-eslint/recommended-type-checked
# or
plugin:@typescript-eslint/strict-type-checked
```

3. Optionally add:

```bash
plugin:@typescript-eslint/stylistic-type-checked
```

4. Install eslint-plugin-react and update the ESLint extends list:

```bash
npm install eslint-plugin-react
# or
yarn add eslint-plugin-react
```

In your ESLint configuration file:

```json
{
  "extends": [
    "plugin:react/recommended",
    "plugin:react/jsx-runtime"
  ]
}
```

### Available Scripts

- `npm run dev` or `yarn dev`: Start the development server.
- `npm run build` or `yarn build`: Build the application for production.
- `npm run serve` or `yarn serve`: Serve the production build.
- `npm run lint` or `yarn lint`: Lint the codebase.
