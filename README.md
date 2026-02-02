# Tinkerbell

For complete documentation visit [tinkerbell.org](https://tinkerbell.org/)

Tinkerbell is a bare metal provisioning engine.
It’s built and maintained with love by the Tinkerbell Community.

## Contributing

This website uses Hugo to generate static HTML pages.
It's hosted and automatically build by Netlify (see [netlify.toml](./netlify.toml "View file") for more details).

- [`content/`](./content/ "View the directory") directory contains documentation files
- [`hugo.toml`](./hugo.toml "View file") is the Hugo configuration
- [`netlify.toml`](./netlify.toml "View file") is Netlify configuration

### Build the site locally

Clone the repository:

```sh
git clone https://github.com/tinkerbell/tinkerbell.org
cd tinkerbell.org
```

#### Using Netlify CLI (recommended)

The Netlify CLI provides the most accurate local preview, including support for redirects defined in `netlify.toml`.

1. Install the [Netlify CLI](https://docs.netlify.com/cli/get-started/):

   ```sh
   npm install -g netlify-cli
   ```

2. Start the development server:

   ```sh
   netlify dev
   ```

Site can be viewed at [http://localhost:8888](http://localhost:8888)

#### Using Hugo directly

Alternatively, you can use Hugo directly. Note that some features like redirects may not work identically to production.

1. Install [Hugo](https://gohugo.io/getting-started/installing/) (v0.155.1 or later)

2. Start the development server:

   ```sh
   hugo server -D
   ```

Site can be viewed at [http://localhost:1313](http://localhost:1313)

### Making changes

#### Adding a new documentation page

```sh
# example: adding new documentation page under section
hugo new section/name-of-new-page.md
```

#### Modifying an existing documentation page

Find the documentation page file (`.md` file) under `content/` and edit it.

### Publishing your changes

[Create a Pull Request](https://help.github.com/en/articles/creating-a-pull-request) with your changes.
When the PR is merged site will be updated automatically by Netlify.

## Licensing

The code snippets and the documentation is licensed under Apache license.
See [LICENSE](./LICENSE) for the full license text.
