# pmd
Write documentation for Python projects in Markdown.

This is just a space where I can write down my ideas for how I would like to write Python docs.

## Outputs

HTML output is the obvious choice but PDF might also be useful. If we were to implement something like a search feature then we would also need to host the docs somehow. I think Sphinx has some kind of JS based search feature where the index is compiled and sent to the browser.

## Separated Documentation

Write some markdown files in a `docs/` directory and have `pmd` compile them together.

## Docstrings

Write markdown in docstrings and have `pmd` pull that into the generated docs.

## Links

Intelligently discover where links were supposed to point to and display a nicely formatted bit of text. For example write `[myproject.subpackage.module.class:function]` to create a link to that particular function that looks like `[function](myproject.subpackage.module.class:function)` when rendered. Or `[filename.md]` to link to a particular file.

## Structure

Define structure using file hierachy in docs directory. Don't requre a TOC, auto-generate one.

`docs/api/` would have to be a protected namespace for the auto-generated code docs.

## Usage

Have a set of config values that have sensible defaults, can be set using a config file and overridden using the command line.

    pmd build --format=html --docs-dir=./docs --build-dir=./docs/_build --auto-doc=mypackage --auto-doc=datetime.date
    pmd serve
