---
search:
  exclude: true         # Removes this page/file from the search index
status: new
---

## Installation Process

???+ tip "For More Details"
    - Comprehensive details can be found at:
        * [`mkdocs` docs](https://www.mkdocs.org/getting-started/ "The getting started guide for `mkdocs`")
        * [material docs](https://squidfunk.github.io/mkdocs-material/ "The homepage for the `materials` theme + framework")
        * [PyMdown extensions doc](https://facelessuser.github.io/pymdown-extensions/ "The homepage for the PyMdown extensions")


The following terminal commands will guide you in setting up and running `mkdocs` locally.
<div class="annotate" markdown>
1. `python3 -m venv venv` - Create a virtual environment entitled 'venv'.
2. `source venv/bin/activate` - Activate the 'venv' virtual environment.
3. `pip install --upgrade pip` - Upgrade `pip`.
4. `pip install mkdocs-material` - The theme I chose to use, further details can be found [here](https://squidfunk.github.io/mkdocs-material/ "The homepage for the `materials` theme + framework")(1).
5. `pip install mkdocs-glightbox` - Install for zoom functionality with images, further details can be found [here](https://blueswen.github.io/mkdocs-glightbox/ "The homepage for a MkDocs plugin to support image lightbox with GLightbox.").
6. `cd [dir-name]` - Assuming the folder for mkdocs, `dir-name` has been created, enter it(2).
7. `mkdocs serve` - Run this command to load mkdocs and preview site as you write.
</div>
1.  `pip install mkdocs` - This command will install `mkdocs`, but is not needed as `pip install mkdocs-material` will handle it for you.
2.  If the folder does not exist, first create it with `mkdocs new [dir-name]` then run the `cd`  command.

???+ note "Remember"
    * The dev-server also supports auto-reloading, and will rebuild your documentation whenever anything in the configuration file, documentation directory, or theme directory changes. This will lead to ease in editing.
    * Files and directories with names which begin with a dot (for example: .foo.md or .bar/baz.md) are ignored by MkDocs. This can be overridden with the exclude_docs config.

## Other Useful Commands
- mkdocs
    - `mkdocs new [dir-name]` - Create a new project.
    - `mkdocs serve` - Start the live-reloading docs server.
    - `mkdocs build` - Build the documentation site.
    - `mkdocs -h` - Print help message and exit.
- mkdocs-material
    - `pip show mkdocs-material` - Show the currently installed version
    - `pip install --upgrade --force-reinstall mkdocs-material` - Upgrade to the latest version



## Useful Formatting Details

* [Admonitions](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#admonitions "Admonitions Reference Guide")
    - They are [twelve built-in types](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#supported-types) of admonitions which may be used.

* [Images](https://squidfunk.github.io/mkdocs-material/reference/images/#images "Images Reference Guide")
    - We have installed `glightbox` for `mkdocs`, use their syntax found [here](https://blueswen.github.io/mkdocs-glightbox/ "MkDocs GLightbox Reference Guide").

![Image title](https://dummyimage.com/600x400/eee/aaa){ data-title="Example Title" data-description="Some description text" data-caption-position="right"}

* [Page Status](https://squidfunk.github.io/mkdocs-material/reference/#setting-the-page-status "Setting the Page Status")

* [Content Tabs](https://squidfunk.github.io/mkdocs-material/reference/content-tabs/#content-tabs "Content Tabs Reference Guide")

=== "BC 100"

    * BC 100 Specific details

=== "Flatbed"

    * Flatbed specific details


### Test


## To Do

- Add [`- navigation.indexes`](https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/#section-index-pages) along with file layout to improve site flow.
- Add [feedback widget](https://squidfunk.github.io/mkdocs-material/setup/setting-up-site-analytics/#was-this-page-helpful) to capture any issues with documentation, but it requires a third party plugin.
- Confirm if we must distribute the site offline, which may be done via this [`offline plugin`](https://squidfunk.github.io/mkdocs-material/setup/building-for-offline-usage/#built-in-offline-plugin).
- Confirm if documentation should have versioning. If so, consider if to use [`mike`](https://squidfunk.github.io/mkdocs-material/setup/setting-up-versioning/#setting-up-versioning).


