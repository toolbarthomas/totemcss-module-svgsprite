# Totemcss module: SVG Sprite
Twig partial for outputting SVG Sprite in your document.

This module is created for [Totemcss](https://www.github.com/toolbarthomas/totemcss) projects but can also be used in any other Twig related project.

## Installation

Install totemcss-module-svgsprite with [npm](https://www.npmjs.com/) (we assume you have pre-installed [node.js](https://nodejs.org/)).

```bash
$ npm install totemcss-module-svgsprite --save
```

## How to include svg-sprite-injector.twig
In the following example we will include svg-sprite-injector.twig from our default page.
You can define a svg sprite (parameter **svg_sprite**) and the base directory (parameter: **base**).

### Source

```twig
<body>
    ...
    {% include 'node_modules/totemcss-module-svgsprite/partials/svg-sprite-injector.twig' with {
        svg_sprite: '/totemcss/main/img/layout/svgsprite.svg'
        revision: false
    } %}
    ...
</body>
```


### Result:

```html
<script>
    !function (e, t) {...}()); /* svg-sprite-injector.min.js */
</script>
<script>
    svgSpriteInjector("/totemcss/main/images/layout/svg-sprite.svg", {
        revision: '2017-11-02--17:25:24')) // Will be the current timestamp
    });
</script>

```

## Svg Sprite Injector
This module uses the original SVG Sprite injector package created by Bogdan Chadkin.
Any bugs related to the actual SVG Sprite Injector should be reported at it's [Github Repository](https://github.com/TrySound/svg-sprite-injector/issues)
