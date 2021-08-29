![alt text](https://github.com/dgarcia360/openapi-boilerplate/blob/master/docs/header.png?raw=true)

# OpenAPI Boilerplate

![build](https://github.com/dgarcia360/openapi-boilerplate/workflows/build/badge.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A starter template for **OpenAPI Specification** projects.

This project breaks the [Swagger Petstore](https://petstore.swagger.io/) example from the official documentation into smaller files. It also adds some handy commands to build, lint, and preview the OpenAPI specification from the command-line.

## Features

* 📝 Write OpenAPI definitions in different files.
* 🔀 Combine all files with [APIDevTools/swagger-cli](https://github.com/APIDevTools/swagger-cli).
* ✅ Validate and lint the OAS document with [stoplight/spectral](https://github.com/stoplight/spectral)
* ✨ Publish reference docs with  [redocly/redoc](https://github.com/Redocly/redoc) & GitHub pages

## Why?

I have defined several OpenAPI specifications recently. But, I always ended with large OpenAPI documents, which were a nightmare to maintain.

So I made this opinionated starter template to define, test, and publish modular OpenAPI specifications. Either if you want to create a new OpenAPI document from scratch or you already have it defined, you can use this template to guide the organization of your project.

## Getting Started

### Requirements

* Node.js 14 LTS

### Installation

1. Clone the repository.

```
git clone https://github.com/dgarcia360/openapi-boilerplate.git
```

2. Install the project dependencies.

```
npm install
```

3. Edit ```openapi.yaml``` to fit your API definition. If you are not familiar with the OpenAPI Specification, it's worth taking a look first to the [documentation](https://swagger.io/solutions/getting-started-with-oas/).

## Useful Commands

### Build

The command bundles the spec as one ``.yaml`` file.

```
npm run build
```

The minified document is stored in ``_build/openapi.yaml``.

### Test

The command checks if the document follows the OpenAPI 3.0 Specification.

```
npm run test
```

### Preview

The command builds a docs site so that you can view the rendering on your local browser.

```
npm run preview
```

The server starts on http://127.0.0.1:8080

## Ready-to-Use Workflows

The project uses [GitHub Actions](https://github.com/features/actions) for Continous Integration.

On every new pull request, the OpenAPI document is linted with [spectral](https://github.com/stoplightio/spectral). If there are changes that introduce errors, the bot will highlight them replying to the pull request.

When the default branch (``master``) receives an update, a workflow automatically publishes the API reference documentation site to GitHub Pages. The site is generated with [ReDoc](https://github.com/Redocly/redoc).

See ``.github/workflows`` to customize the available workflows. If you don't plan to use GitHub to host your spec or prefer to keep docs private, delete the ``.github`` folder.

## Contributing

Contributions are welcome and appreciated! 
If you want to enhance the boilerplate, please read [CONTRIBUTING.md](CONTRIBUTING.md) file first.

## License

Copyright (c) 2019-present David Garcia ([@dgarcia360](https://davidgarcia.dev)). Licensed under the [MIT License](LICENSE.md).

The PetStore example used is derived from [OAI/OpenAPI-Specification](https://github.com/OAI/OpenAPI-Specification/blob/master/examples/v3.0/petstore.yaml), Copyright The Linux Foundation, Licensed under the [Apache License, Version 2.0](https://github.com/OAI/OpenAPI-Specification/blob/master/LICENSE).
