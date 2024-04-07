---
search:
  exclude: true
---

## Installation Process
Comprehensive details can be found at:

- [`mkdocs` getting started guide](https://www.mkdocs.org/getting-started/)
- [material theme](https://squidfunk.github.io/mkdocs-material/)


The following terminal commands will guide you in setting up and running `mkdocs` locally.

1. `python3 -m venv venv` - Create a virtual environment entitled 'venv'.
2. `source venv/bin/activate` - Activate the 'venv' virtual environment.
3. `pip install --upgrade pip` - Upgrade `pip`.
4. `pip install mkdocs-material` - The theme I chose to use, further details can be found [here](https://squidfunk.github.io/mkdocs-material/).
    - `pip install mkdocs` - This will install `mkdocs`, but is not needed as `pip install mkdocs-material` will handle it for you.
5. `cd [dir-name]` - Assuming the folder for mkdocs, `dir-name` has been created, enter it.
    - If the folder does not exist, first create it with `mkdocs new [dir-name]` then run the `cd`  command.
6. `mkdocs serve` - Run this command to load mkdocs and preview site as you write.

Remember,
> The dev-server also supports auto-reloading, and will rebuild your documentation whenever anything in the configuration file, documentation directory, or theme directory changes.

This will lead to ease in editing.

Also,
> Files and directories with names which begin with a dot (for example: .foo.md or .bar/baz.md) are ignored by MkDocs. This can be overridden with the exclude_docs config.

## Other Useful Commands
- mkdocs
    - `mkdocs new [dir-name]` - Create a new project.
    - `mkdocs serve` - Start the live-reloading docs server.
    - `mkdocs build` - Build the documentation site.
    - `mkdocs -h` - Print help message and exit.
- mkdocs-material
    - `pip show mkdocs-material` - Show the currently installed version
    - `pip install --upgrade --force-reinstall mkdocs-material` - Upgrade to the latest version

## To Do

- Add [`- navigation.indexes`](https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/#section-index-pages) along with file layout to improve site flow.
- Add [feedback widget](https://squidfunk.github.io/mkdocs-material/setup/setting-up-site-analytics/#was-this-page-helpful) to capture any issues with documentation, but it requires a third party plugin.
- Confirm if we must distribute the site offline, which may be done via this [`offline plugin`](https://squidfunk.github.io/mkdocs-material/setup/building-for-offline-usage/#built-in-offline-plugin)