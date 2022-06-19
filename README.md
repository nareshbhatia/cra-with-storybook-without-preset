# CRA with Storybook without preset-create-react-app

This project was bootstrapped with
[Create React App](https://github.com/facebook/create-react-app).

## How was Storybook initialized

```shell
npx sb init --help

Usage: sb init [options]

Initialize Storybook into your project.

Options:
  -f --force                                       Force add Storybook
  -s --skip-install                                Skip installing deps
  -N --use-npm                                     Use npm to install deps
  -p --parser <babel | babylon | flow | ts | tsx>  jscodeshift parser
  -t --type <type>                                 Add Storybook for a specific project type
  -y --yes                                         Answer yes to all prompts
  -b --builder <builder>                           Builder library
  -l --linkable                                    Prepare installation for link (contributor helper)
  -h, --help                                       display help for command
```

Ran sb init with following options:

```shell
npx sb init --skip-install --type react --builder webpack5
```

The added the following overrides in `package.json`:

```json
{
  "overrides": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-refresh": "0.13.0"
  }
}
```

## Running Storybook

```shell
npm run storybook
```

## Running the app

```shell
npm start
```

