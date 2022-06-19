# CRA with Storybook without preset

This project was bootstrapped with
[Create React App](https://github.com/facebook/create-react-app).

## How Storybook was initialized

To list available options, start `sb init` with the `--help` option:

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

Storybook was added using `sb init` with the following options. This prevents
`sb init` from automatically detecting the application type (in this case CRA).
We explicitly ask for application type react and the webpack5 builder.

```shell
npx sb init --skip-install --type react --builder webpack5
```

After this I had to add the following overrides to `package.json` to overcome
dependency conflicts:

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
