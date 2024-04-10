---
search:
  exclude: true         # Removes this page/file from the search index
status: new
---

The following is a brief explanation for using `mkdocs` coupled with `mkdocs-material` for the creation of documentation.

???+ tip "For More Details"
    - Comprehensive details can be found at:
        * [`mkdocs` docs](https://www.mkdocs.org/getting-started/ "The getting started guide for `mkdocs`")
        * [Material docs](https://squidfunk.github.io/mkdocs-material/ "The homepage for the `materials` theme + framework")
        * [PyMdown extensions docs](https://facelessuser.github.io/pymdown-extensions/ "The homepage for the PyMdown extensions")
        * [Lightbox for `mkodcs` docs](https://blueswen.github.io/mkdocs-glightbox/)


## Installation Process

Before using `mkdocs`, be sure to use the following steps.

The following terminal commands will guide you in setting up and running `mkdocs` locally.
<div class="annotate" markdown>
1. `python3 -m venv venv` - Create a virtual environment entitled 'venv'.
2. `source venv/bin/activate` - Activate the 'venv' virtual environment.
3. `pip install --upgrade pip` - Upgrade `pip`.
4. `pip install mkdocs-material` - The chosen [theme](https://squidfunk.github.io/mkdocs-material/ "The homepage for the `materials` theme + framework")(1).
5. `pip install mkdocs-glightbox` - Install for zoom functionality with images, further details can be found [here](https://blueswen.github.io/mkdocs-glightbox/ "The homepage for a MkDocs plugin to support image lightbox with GLightbox.").
6. `cd [dir-name]` - Assuming the folder for mkdocs, `dir-name` has been created, enter it(2).
7. `mkdocs serve` - Run this command to load mkdocs and preview site as you write and save your files.
</div>
1.  `pip install mkdocs-material` will handle install the theme, `mk-docs` and usefule extension packages. If only `mkdocs` is required, use just the command `pip install mkdocs`.
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


## YAML Configuration

The generated website is modified through the use of a yaml file, typically named `mkdocs.yml` in this file you can modify the following:

- Project Information
- Page Tree
- Extensibility (Plugins & Extensions)


## Useful Formatting Details

When formatting your markdown files, it may be useful to refer to the [references](https://squidfunk.github.io/mkdocs-material/reference/ "Overview of References in material theme") to see wht is possible, but highlighted below are an opinionated subset of what may give the most mileage in general.

### [Admonitions](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#admonitions "Admonitions Reference Guide")

They are [twelve built-in types](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#supported-types) of admonitions which may be used. as a form of highlighting information.

See below for an example of how to write a note and how it would be rendered.

=== "Format of Note"
    !!! quote ""
        ```md
            !!! note "Title"
                This is a note.
        ```
=== "Render of Note"
    !!! note "Title"
        This is a note.

### [Images](https://squidfunk.github.io/mkdocs-material/reference/images/#images "Images Reference Guide")


As we have installed `glightbox` for `mkdocs`, use their syntax which can be found [here](https://blueswen.github.io/mkdocs-glightbox/ "MkDocs GLightbox Reference Guide").

See below for an example of how to write the details for an image and how it would be rendered.


=== "Image with inline descriptor"
    ```md
    ![Image title](https://dummyimage.com/600x400/eee/aaa){ data-title="Example Title" data-description="Some description text" data-caption-position="right"}
    ```
=== "Image with html descriptor"
    ```md
    <figure markdown>
    ![Image title](https://dummyimage.com/600x400/eee/aaa){ data-title="Example Title" data-description=".custom-desc1" data-caption-position="right"}
    <figcaption>Example Title</figcaption>
    </figure>
    <div class="glightbox-desc custom-desc1">
    <p>Some description text</p>
    </div>
    ```
=== "Rendered Image"
    <figure markdown>
    ![Image title](https://dummyimage.com/600x400/eee/aaa){ data-title="Example Title" data-description=".custom-desc1" data-caption-position="right"}
    <figcaption>Example Title</figcaption>
    </figure>
    <div class="glightbox-desc custom-desc1">
    <p>Some description text</p>
    </div>



### [Content Tabs](https://squidfunk.github.io/mkdocs-material/reference/content-tabs/#content-tabs "Content Tabs Reference Guide")

The following is how to insert content into tabs.

=== "Text for Tabs"
    ```md
        === "BC 100"
            * BC 100 Specific details
        === "Flatbed"
            * Flatbed specific details
    ```
=== "Render of Tabs"
    === "BC 100"
        * BC 100 Specific details
    === "Flatbed"
        * Flatbed specific details




### [Page Status](https://squidfunk.github.io/mkdocs-material/reference/#setting-the-page-status "Setting the Page Status")

There may be times when it's necessary to highlight certain pages and aside from a change log, the use of a page status may be prefferred. This current page has used one, please see the logo.

This was done by placing the following at the top of the file.

```md
    ---
    status: new
    ---
```

## To Do

- Add [`- navigation.indexes`](https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/#section-index-pages) along with file layout to improve site flow.
- Add [feedback widget](https://squidfunk.github.io/mkdocs-material/setup/setting-up-site-analytics/#was-this-page-helpful) to capture any issues with documentation, but it requires a third party plugin.
- Confirm if we must distribute the site offline, which may be done via this [`offline plugin`](https://squidfunk.github.io/mkdocs-material/setup/building-for-offline-usage/#built-in-offline-plugin).
- Confirm if documentation should have versioning. If so, consider if to use [`mike`](https://squidfunk.github.io/mkdocs-material/setup/setting-up-versioning/#setting-up-versioning).


