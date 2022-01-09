# Turborepo Boiler Plate

- Includes Next.js, Remix, Expo, and React Native projects
  - apps
    - web: Next.js
    - docs: Next.js
    - blog: Remix
    - rnative: React Native
      - @react-navigation/native-stack example
  - packages
    - ui: react lib
    - ui-native: react-native lib
  - wrappers
    - bp-request: sample js wrapper lib for axios

# How to use

### NOTE FOR REACT NATIVE:

1. In the scripts of `apps/rnative/package.json` you will want to make sure that `dev` is set to run either ios or android depending on your setup. By default it runs
   ios.

```
apps/rnative/package.json

scripts": {
    "dev": "yarn ios", // yarn ios | yarn android | yarn start
    "android": "react-native run-android",
    "ios": "react-native run-ios",
    "start": "react-native start",
    "test": "jest",
    "lint": "eslint . --ext .js,.jsx,.ts,.tsx",
    "clean": "rm -rf .turbo && rm -rf node_modules"
  },
```

### Run commands:

`yarn dev` runs all the projects in a development state as this project copies the kitchen-sink example from turbo. You will want to edit the `dev` command of a project's `package.json` to do something else or remote it entirely. You may want look at Turbo's docs under --scope for more control.

- Clone: `git clone https://github.com/Enricopv/turbo-boilerplate.git {name}`
- Install: `yarn`
- Run: `yarn dev` // to run all projects
- Run: `yarn dev --scope={name}` // to run a single project. Running this may not show your live updates from the ui packages if they are not also running too.

## Troubleshooting

<b>Long jest-haste-map Issue</b>

- If you are running into ths problem, try running `yarn clean:watchman`.
