# VeamsTemplater Plugin

This plugin adds the possibility to render your `handlebars` templates in an easy way. You can register the engine, templates, partials and helpers and use them directly in your other classes.

### How to

``` js
import Veams from 'veams';
import VeamsTemplater from 'veams-plugin-templater';
import handlebars from 'handlebars/runtime';
import { templates, partials } from './templates';
import { customHelper } from './helpers';

// Add plugins to the Veams system
Veams.use(VeamsTemplater, {
    engine: handlebars,
    templates: templates,
    partials: partials,
    helpers: [
        customHelper
    ]
});

// Render the template
$(body).append(
    Veams.templater.render('_test-partial', {data: 'custom data passed to partial'})
);

```
