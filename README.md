Mannequin HTML is brought to you by your friends at [Last Call Media](https://www.lastcallmedia.com), it is a command line application that you can use to visualize and work on your static HTML files in the browser. For example, if you have a directory of separate HTML files that represent the "components" of your application, you can use Mannequin HTML to view and work on them individually.

Quick Start
-----------
Using [Composer](https://getcomposer.org/doc/00-intro.md), install Mannequin HTML from your project root.  From the command line:
```bash
$ composer require lastcall/mannequin-html
```
Next, create a new `.mannequin.php` file in your project root.  This file is where you will configure Mannequin.  Inside of that file:

[@see config](demo/.mannequin.php#L23-50)

See all of the [configuration options](docs/configuration.md), or [view an example project](demo/)

Setting up Components
---------------------
While the `.mannequin.php` file tells Mannequin where to find your components, you still need to describe them to Mannequin.  To do that, we use a `.yml` file living alongside the `.html` file that contains the component.  For example, to describe a "Card" component living inside of `card.html`, you would create a `card.yml` file in the same directory that contains:
```yaml
# card.yml
name: Card
group: Molecule
```
See the full YAML reference [here](docs/components.md)

Workflow
--------

When you're ready to begin work on your HTML files, you can use the following worklow:

1. Fire up a live development server so you can see your component.  From the command line:
    ```bash
    $ vendor/bin/mannequin start
    ```
2. This will output a URL for the Mannequin UI.  Visit it in your browser.
3. In the UI, find the component you want to work on.
4. Open the HTML file, and make your changes.
5. Reload the UI to see how your changes look.
