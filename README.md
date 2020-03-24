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
