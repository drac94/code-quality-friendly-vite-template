# Code Quality Friendly Vite Template

![tools included](https://user-images.githubusercontent.com/1719915/190883201-4a4aac05-2eaa-4886-b8f0-3a7de1a38ffa.png)

This template includes:

- [Typescript](https://www.typescriptlang.org/)
- [ESLint](https://eslint.org/docs/user-guide/getting-started)
- [Prettier](https://prettier.io/)
- [Husky](https://github.com/typicode/husky)
- [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/)

### Path alias ~/

- Context: https://twitter.com/domhabersack/status/1557763450687848448

### ESlint Rules

#### Prefer Array\<T> over T[]

- Rule: [array-type](https://typescript-eslint.io/rules/array-type/)
- Why: https://twitter.com/TkDodo/status/1352201629408387072

#### Don't allow unused variables unless they start with an underscore

- Rule: [no-unused-vars](https://typescript-eslint.io/rules/no-unused-vars)
- Why: Unused variables are removed from the prod build, but can make the code harder to read. There are times when you need to declare them though, like in event handlers where the event parameter isn't needed but is required, so the rule allows you to declare those variables using an underscore.

```jsx
const handleEvent = (_event, data) => {};
```

#### Ordered imports

- Rule: [import/order](https://github.com/import-js/eslint-plugin-import/blob/main/docs/rules/order.md)
- Why: Ordered and grouped imports helps to avoid conflicts when several people add new imports to the same file.

#### No React import in JSX file unless is needed

- Rule: [react-in-jsx-scope](https://github.com/jsx-eslint/eslint-plugin-react/blob/master/docs/rules/react-in-jsx-scope.md)
- Why: Starting with React 17 it is not needed to import React at the top of the JSX files. Source: https://reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html

#### Prefer arrow functions

- Rule: [eslint-plugin-prefer-arrow-functions](https://github.com/JamieMason/eslint-plugin-prefer-arrow-functions)
- Why: I hate _this_
- Note: This is more a preference, you can deactivate it by removing line 30 and 79-87 in the `.eslintrc` file and running the following command

```sh
yarn remove eslint-plugin-prefer-arrow-functions
```
