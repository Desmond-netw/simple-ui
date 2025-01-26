# Simple UI Component creating

## Use Vite + React

Packages and libraries used include

- Vitest
- Storybook
- Tailwind css
- Clsx
- chakra : https://v2.chakra-ui.com/docs/components/button/usage
- cva : class variance authority library
- tailwindcss merge

  ## \*\*Environment Setup

  \*\* file > vite.config.js

```js
import tailwindcss from "@tailwindcss/vite";
import { defineConfig } from "vite";

// https://vite.dev/config/
export default defineConfig({
  plugins: [tailwindcss()],
});
```

\*\* directory > .vscode > settings.json

```json
{
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit",
    "source.organizeImports": "explicit"
  },
  "editor.formatOnSave": true, //tell vscode to format files on save
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.snippetSuggestions": "inline"
}
```

\*\* configure the story book main.ts file after installing story book
add this after the main code

```ts
....
docs: {
    autodocs: "tag",
  },
  viteFinal: async (config) => {
    config.plugins?.push(
      /** @see https://github.com/aleclarson/vite-tsconfig-paths */
      tsconfigPaths({
        projects: [path.resolve(path.dirname(__dirname), "tsconfig.json")],
      })
    );
    return config;
  },
  ...
```

- In story .storybook > priview.ts add the following to point to the css, or the tailwind css. example can be

* ```ts
  import "../src/App.css";
  ```

```

```
