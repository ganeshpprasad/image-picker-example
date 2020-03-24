#Steps followed

```
react-native init projectName
yarn add --dev typescript react-native-typesctipt-transformer
yarn tsc --init --pretty --jsx react-native
```

Transform ts

```
touch rn-cli.config.js
```

add ->

```
module.exports = {
  getTransformModulePath() {
    return require.resolve('react-native-typescript-transformer');
  },
  getSourceExts() {
    return ['ts', 'tsx'];
  },
};

```

```
yarn add --dev @types/react @types/react-native
```

Testing

```
yarn add --dev ts-jest
```

package.json

```
 "moduleFileExtensions": [
      "ts",
      "tsx",
      "js"
    ],
    "transform": {
      "^.+\\.(js)$": "<rootDir>/node_modules/babel-jest",
      "\\.(ts|tsx)$": "<rootDir>/node_modules/ts-jest/preprocessor.js"
    },
    "testRegex": "(/__tests__/.*|\\.(test|spec))\\.(ts|tsx|js)$",
    "testPathIgnorePatterns": [
      "\\.snap$",
      "<rootDir>/node_modules/"
    ],
    "cacheDirectory": ".jest/cache"
```

```
yarn add --dev @types/jest @types/react @types/react-native @types/react-test-renderer
```
