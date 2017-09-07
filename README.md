# VeamsTemplater Plugin

This plugin adds the possibility to render your `handlebars` templates in an easy way. You can register the engine, templates, partials and helpers and use them directly in your other classes.

### How to

```js
import Veams from 'veams';
import VeamsVent from 'veams-plugin-templater';
import handlebars from 'handlebars';
import { templates, partials } from './templates';
import { customHelper } from './helpers';


// Intialize core of Veams
Veams.initialize();

// Add plugins to the Veams system
Veams.use(VeamsTemplater, {
    engine: handlebars,
    templates: templates,
    partials: partials,
    helpers: [
        customHelper
    ]
});
```
