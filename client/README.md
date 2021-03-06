# Project Skeleton Client

The client was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app) (CRA) and includes all of capabilities provided by CRA. Some built-in functionality of that skeleton was stripped out, specifically the [offline caching](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app).

## Setup

You should install the dependencies from the "top-level" package as described in its README or via `npm install` in this directory.

The development server will attempt to proxy API requests to the server specified in the `package.json` "proxy" field. The application has been configured to proxy requests to the associated server at http://localhost:3001.

## Development

### Component Library

The [`Form` component](src/components/Form.js) is developed using [Material UI](https://material-ui.com/). Material UI is a Framework on top of react for building more robust and user friendly components. The component library obviates the need for tedious and monotonous UI development and instead lets devolopers focus on higher level conceptual tasks, such as how individual components should be built with respect to the application architecture.

For more inofrmation on Material UI components, check out their [documentation](https://material-ui.com/getting-started/usage/).

### Testing

The tests use both Jest and Enzyme has described in the [CRA documentation](https://facebook.github.io/create-react-app/docs/running-tests).

For reference Enzyme was installed with:

```
npm install --save-dev enzyme enzyme-adapter-react-16 react-test-renderer
```

### Linting

You can run the linter with `npm run lint` or `npx eslint .`. Include the `--fix` option to `eslint` to automatically fix many formatting errors, e.g. `npm run lint -- --fix`, although note that the "fix" option can introduce errors so we recommended committing beforehand.

For reference a custom ESLint configuration is provided as described in the top-level README. We installed the Prettier ESlint configuration to prevent conflicts with that tool via

```
npm install --save-dev eslint-config-prettier
```

and updated the `.eslintrc.json` configuration to be:

```
{
  "extends": ["react-app", "prettier"],
  "rules": {
    ... Many rules adapted from AirBnB style guide
  }
}
```
