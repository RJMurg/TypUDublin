# TypUDublin
This thesis template is derived from the [TypXidian](https://github.com/angelonazzaro/typxidian) template.
It is modified to be similar to the standard TU Dublin thesis template.

## Usage

It is best you become knowledgeable with Typst syntax.

For other specifics to leverage the power of this template, look at TypXidian's repository for the additional things you can do!

You will also need to add a photo of your signature in the figures directory. It defaults to an image called signature.svg, but can be changed by adding `declaration-signature:` to the template.with in `report.typ`

The VS Code extension Tinymist Typist should be installed. Every time you open VS Code, open `report.typ`, then press `CMD/CTRL + SHIFT + P` to open the Command Pallette and then run Pin the Main File to the Currently Open Document. This will handle word-count and Intellisense support.

To run automatic building, open a VS Code terminal and run `typst watch report.typ` which will automatically rebuild the PDF whenever a file is saved.

It is neater to split your chapters into separate files, the `chapters/` directory already exists for this. Do not forget to import new chapters in `report.typ`.

Any images should be included in the `figures/` directory, and can be imported with `#image()`.
Figures can automatically handle tables and images, and these will be automatically added to the Table of Figures and Table of Tables at the end of the document automatically. If you want to figure a code block, you will need to specify kind. I.e.:
```typst
#figure(
  ```python
  print("Hello World!")
  ```,
  kind: image,
  caption: "A Hello World program in Python."
)
```


## Requirements

To work with TypUDublin you will need:

- [Typst](https://typst.app/) version 0.13.1 or newer
- Optionally, a `.bib` file if you want to manage your bibliography
- Optionally, an `abbreviations.typ` file if your document uses acronyms
- The template also makes use of Font Awesome icons via the [fontawesome](https://typst.app/universe/package/fontawesome) package.
  For these to display correctly, you should install the [Font Awesome 7 Desktop](https://fontawesome.com/download) fonts on your computer,
  or upload them to your project folder if you are working on the Typst web app.

## License

TypUDublin is distributed under the MIT License.