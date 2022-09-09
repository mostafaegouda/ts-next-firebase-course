# Next.js + Firebase - The Full Course

### `TypeScript - Firebase v9 - Next.js v12.3`

----------------

## Guide

Next.js v12.3 comes with a great new quality of life improvment. When a changing javascript project into typescript, it auto installs typescript and config files after changing any `.js` or `.jsx` file to `.ts` or `.tsx`

### Setup

Run `npm run dev` then change `_app.js` file to `_app.tsx`.

You will notice next js installs typescript and creates 2 new files: `tsconfig.json` and `next-env.d.ts`.

Copy the config options under `"compilerOptions"` in `jsconfig.json` to the `tsconfig.json` below `"jsx": "preserve",`.

Now we can safely delete `jsconfig.json`.

Make sure to change `"strict": true` to `"strict": false` in `tsconfig.json`.


`tsconfig.json`

```
{
  "compilerOptions": {
    "target": "es5",
    "lib": [
      "dom",
      "dom.iterable",
      "esnext"
    ],
    "allowJs": true,
    "skipLibCheck": true,
    "strict": true,
    "forceConsistentCasingInFileNames": true,
    "noEmit": true,
    "incremental": true,
    "esModuleInterop": true,
    "module": "esnext",
    "moduleResolution": "node",
    "resolveJsonModule": true,
    "isolatedModules": true,
    "jsx": "preserve",
    "baseUrl": "./",
      "paths": {
        "@components/*": ["components/*"],
        "@styles/*": ["styles/*"],
        "@lib/*": ["lib/*"],
      }
  },
  "include": [
    "next-env.d.ts",
    "**/*.ts",
    "**/*.tsx"
  ],
  "exclude": [
    "node_modules"
  ]
}
```