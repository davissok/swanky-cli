# Swanky templates

Templates used to generate Swanky projects and `ink!` language contracts.
Templates are parsed using [Handlebars](https://handlebarsjs.com/) templating engine, and are passed the following object:

```ts
{
  project_name: string;
  author_name: string;
  author_email: string | undefined;
  swanky_version: string;
  contract_name: string;
  contract_name_snake: string;
  contract_name_pascal: string;
}
```

## Project templates

General config templates used by every generated project:

- `config.json.hbs`: config used by typechain
- `package.json.hbs`
- `tsconfig.json`
- `gitignore`

## Contract templates

Each contract directory must contain `contract` and `tests` subdirectories.

All the files contained within will be copied, respecting the directory structure, and the `.hbs` files will be processed by the templating engine.
