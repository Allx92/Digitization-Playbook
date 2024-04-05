

## Installation Process
Comprehensive details can be found at
- [`mkdocs` getting started guide](https://www.mkdocs.org/getting-started/)
- [material theme](https://squidfunk.github.io/mkdocs-material/)

The following terminal commands will guide you in setting up and running `mkdocs` locally.

1. `python3 -m venv venv` - Create a virtual environment entitled 'venv'.
2. `source venv/bin/activate` - Activate the 'venv' virtual environment.
3. `pip install --upgrade pip` - Upgrade `pip`.
4. `pip install mkdocs` - Install the `mkdocs` package.
5. `pip install mkdocs-material` - The theme I chose to use, further details can be found [here](https://squidfunk.github.io/mkdocs-material/).
6. `cd [dir-name]` - Assuming the folder for mkdocs, `dir-name` has been created, enter it.
7. `mkdocs serve` - Run this command to load mkdocs


## Other Useful Commands
- `mkdocs new [dir-name]` - Create a new project.
- `mkdocs serve` - Start the live-reloading docs server.
- `mkdocs build` - Build the documentation site.
- `mkdocs -h` - Print help message and exit.


## To Do

Add [`- navigation.indexes`](https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/#section-index-pages) along with file layout to improve site flow.