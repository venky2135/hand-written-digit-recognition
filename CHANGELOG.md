# [v5.1.0](https://github.com/MyScript/myscript-math-web/tree/v5.1.0)

## Features

- Addition of a new Recognition Assets Builder API to dynamically build text lexicons and math grammars
- Ability to import JJIX Math content
- Style and decoration support in the JIIX exports
- New configuration options for a finer tuning of JIIX exports
- Always connected is now the default mode for better end user experience

## Others

- Udpdate Import jiix with math example



# [v5.0.0](https://github.com/MyScript/myscript-math-web/tree/v5.0.0)

## Features

`myscript-math-web` now supports all the features introduced by the version [4.2.0 of MyScriptJS](https://github.com/MyScript/myscriptjs/tree/v4.2.0).

## Breaking changes

- We are now using Polymer 3. For more details, please refer to the [Polymer documentation](https://www.polymer-project.org/3.0/docs/about_30).

# [v4.1.1](https://github.com/MyScript/myscript-math-web/tree/v4.1.1)

## Bugs fixed
- Documentation and paper buttons colors were not taken into account in Edge.

# [v4.1.0](https://github.com/MyScript/myscript-math-web/tree/v4.1.0)

## Features
- Custom resources / grammar support, upload your custom grammar to modify the recognition behaviour (see the [example](./examples/v4/custom_resources.html)).
- New `penStyleClasses` property. Used to change the theme using classes passed using the `theme` property (see the [example](./examples/non-version-specific/customize_style.html)).
- No more css background if api is set to `V4`.
- No more STIX font import needed as the font is now rendered by the server.
- New `usepointerlisteners` property used to force the pointer events use.

## Breaking changes
In order to be consistent with the native API :
- `importContent()` and `exportContent()` respectively renamed to `import_()` and `export_()`.
- `importInk(strokes)` changed to `pointerEvents(events)`.

## Bug fixed

- Math exports rendering for breaking line was printing \\\\ and not breaking line.

# [v4.0.1](https://github.com/MyScript/myscript-math-web/tree/v4.0.1)

## Bug fixed

- Editor on iOS wasn't working properly due to touch-action: none in CSS not supported in Safari.

# [v4.0.0](https://github.com/MyScript/myscript-math-web/tree/v4.0.0)

## Features
- New events to be notified of editor changes. 
- New `unloaded` flag to control component state. `load` event will be trigger once the editor will be fully loaded.
- New **not mutable** `configuration` attribute. Changing the configuration will clear the underlying editor, all currents strokes and results will be lost. To do it, set `unloaded=true` after changing configuration, and wait for a `load` event.
- New **read-only** `editor` property that allow you to access to the underlying editor object (see [MyScriptJS documentation]() for more details).
- New CSS variables to customize the web-component. See [demo/styling.html](demo/styling.html) as an example.
 
## Breaking changes
- Complete rewrite of the underlying javascript library with ES6 syntax
- Internal design improved to allow extensibility and support of upcoming recognition types. Documentation and illustrating samples to come in next release. 
- Removal of all deprecated attributes and methods
- All events has been renamed. See the [documentation](docs/index.html) to discover new behavior.
- `resulttypes`, `language`, `typeset`, `textparameters`, `mathparameters`, `shapeparameters`, `musicparameters`, `analyzerparameters` are replaced by the unique `configuration` attribute (see [MyScriptJS documentation]() for a complete spec).
- Renamed `timeout` attribute to `recognitiontriggerdelay`
- Renamed `delete()` property to `clear()`
- Changed `ssl` attribute to a `scheme` attribute (i.e. `ssl=true` will be replaced by `scheme=https`)
- `getAvailableLanguages()` have been replaced by a new web-component. You can use it to retrieve the list of available languages for your configuration.

## Bugs
- User can no longer write when an unrecoverable error is detected forcing him to reload the page. See [demo/handle_error.html](demo/handle_error.html) to see how it works.

For more details about attributes, look at the [documentation](docs/index.html).

# [v1.2.3](https://github.com/MyScript/myscript-math-web/tree/v1.2.3)

## Features
- Change colors to fit the new MyScript Developer theme

# [v1.2.2](https://github.com/MyScript/myscript-math-web/tree/v1.2.2)

## Features
- New `strokecolor` attribute to setup/change stroke color settings
- New `strokewidth` attribute to setup/change stroke width settings

## Bugs
- See [MyScriptJS v1.2.2](https://github.com/MyScript/MyScriptJS/tree/v1.2.2) for fixes

# [v1.2.1](https://github.com/MyScript/myscript-math-web/tree/v1.2.1)

## Bugs
- See [MyScriptJS v1.2.1](https://github.com/MyScript/MyScriptJS/tree/v1.2.1) for fixes

# [v1.2.0](https://github.com/MyScript/myscript-math-web/tree/v1.2.0)

## Features
- Mutable `host` attribute
- Mutable `protocol` attribute
- New `latex` output attribute to get LaTeX result
- New `mathml` output attribute to get MathML result
- Replace undo/redo/clear/recognize buttons by the `myscript-common-element` ones
- Replace the error panel by the `myscript-common-element` ones
- Upgrade from Polymer 1.2 to 1.4
- Add docs/demo buttons on component page
- Migration to Katex 0.6.0 (Matrix rendering)
- Add getStats method to get various stats relative to ink in order to help evaluate the myscript cdk usage

## Bugs
- Fixes issue on resize due to CSS
- Explicit default values on documentation 
