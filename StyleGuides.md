# Proposed Style Guide

## General Guidelines

- Install Prettier VS Code extension which would eliminate formatting , spacing , semi-colon issues to a greater extent.
- Ensure CamelCase coding style
- Follow First make it work and then refactor the code according to the coding style guides.
- Please add comments.
- Please remember "Good code is self documenting".

## CSS

```jsx
npm install --save-dev eslint@4.19.1 \
                         eslint-config-pagarme-react \
                         stylelint@8.0.0 \
                         stylelint-config-pagarme-react \
```

- Installing above packages will ensure most of the css style guides.
- All css files should be inside their respective folders with components or have component names as their filenames inside styles folder.
<!-- //CSS files inside the respected folder. or styles folder.-->

## Loops

```jsx
// if using this
if (a == true) result;
// use this
{
  a && result;
}
```

```jsx
// if using this
if(a == true)
    ...
else
    ...
// use this
{a ? ... : ...}
// (conditional)
//   ? truthyClause
//   : falsyClause
```

- Nested ternaries are great but make sure they provide good readability.

## Naming Convention

- Naming of variables should be of same context.

```jsx
//bad
let a = 5;
// good
let ItemNo = 5;
```

## Redux

- Container folder should contain components which are directly interacting with store.
- Components folder should contain components which would not interact directly with the store.

## React

### https://github.com/airbnb/javascript/tree/master/react

- Preferably, use create-react-app , but if you don't, provide a valid reason. Eg. SSR.
- Use cdm for making API calls or use useEffect hook

```jsx
...
componentDidMount()
{
    // make API calls here.
}
...
OR
...
useEffect(() => {
    //API calls here
  });
```

- Follow Single Responsibility Principle.
- Prop drilling is okay for components of 3 levels deep. If it exceeds, use React context API or use Redux.
- Do not mutate the state directly. Use this.setState().
- Donot assign props to state directly unless and until

## GIT

- Commit for every feature.
- Push at EOD.
- Let commit messages be brief and and does not exceed > 10 words.

## We can also follow

- Standard - https://standardjs.com/
  which has got more number of stars in GitHub and used by many big players.
