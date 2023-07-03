# Nx `buildLibsFromSource: false` bug reproduction

## Identification of buildable libs

Run `nx serve my-app` and open [http://127.0.0.1:4200/]() in a browser.

You see that the app uses `packages/my-lib/src/lib/my-lib.tsx`, but it should use `dist/packages/mylib` instead.

## Modifying dependency via `tsconfig.json`

Run `npx patch-package`, then run `nx serve my-app` and open [http://127.0.0.1:4200/]() in a browser.

You see that the app still uses `packages/my-lib/src/lib/my-lib.tsx`.