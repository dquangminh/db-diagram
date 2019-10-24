# Database diagram Angular Sample

**Important note:** When adding db-diagram to component template hierarchy, there is an issue with Angular ViewEncapsulation type.

1. By default, Angular use `ViewEncapsulation.Emulated` to generated id which allow view hierarchy to contain special id attribute match with the imported stylesheet. It's allow Angular to emulate view hierarchy and style similar way to actual Web Component. However the `db-diagram` manipulate the dom hierarchy using native javascript API thus all element managed by `db-diagram` will not contain any special id generated by Angular and it's leading to an issue where element does not match the stylesheet selector. The solution is to add `db-diagram` stylesheet globally in the file `angular.json`.

2. Import or reference to stylesheet in the component work with ``ViewEncapsulation.None`, `ViewEncapsulation.Native` and `ViewEncapsulation.ShadowDom`.

> Be aware that Angular do allow import or reference to style in the component if that stylesheet is already define in file `angular.json`.

> Add stylesheet to `angular.json` work with `ViewEncapsulation.Emulated` and `ViewEncapsulation.None`

## Stylesheet and Icons location

Icons.svg locate at

- [node_modules/@krobkrong/db-diagram/dist/resources/icons.svg](node_modules/@krobkrong/db-diagram/dist/resources/icons.svg)

Stylesheet locate at:

1. [node_modules/@krobkrong/db-diagram/dist/resources/styles/style-dark.css](node_modules/@krobkrong/db-diagram/dist/resources/styles/style-dark.css)
2. [node_modules/@krobkrong/db-diagram/dist/resources/styles/style-light.css](node_modules/@krobkrong/db-diagram/dist/resources/styles/style-light.css)