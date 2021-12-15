# MkDocs Em-Img2Fig Plugin

This [MkDocs](https://www.mkdocs.org) plugin converts markdown encoded images surrounded by two asterisks like

```
*![An image caption](\assets\images\my-image.png)*
```

into 

```html
<figure class="figure-image">
  <img src="\assets\images\my-image.png" alt="An image caption">
  <figcaption>An image caption</figcaption>
</figure>
```

## Credits
This plugin is a fork of the stuebersystems/mkdocs-img2fig-plugin which does not require the two asterisks

## Requirements

This package requires Python >=3.5 and MkDocs version 1.0 or higher.  

## Installation

Install the package with pip:

```cmd
pip install mkdocs-em-img2fig-plugi
```

Enable the plugin in your `mkdocs.yml`:

```yaml
plugins:
    - search
    - autolinks
    - em-img2fig
```
**Note:** If you use autolinks or similar plugin declare em-img2fig after it, not before for correct precedence.

**Note:** If you have no `plugins` entry in your config file yet, you'll likely also want to add the `search` plugin. MkDocs enables it by default if there is no `plugins` entry set, but now you have to enable it explicitly.

More information about plugins in the [MkDocs documentation](https://www.mkdocs.org/user-guide/plugins/)
