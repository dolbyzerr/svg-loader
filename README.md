# svg-loader

Webpack loader that inlines SVG content so that you can control and alter it.
Unlike SVG inserted as an image, svg-loader allows to animate, change color,
control size, etc.

## Installation

```bash
npm install svg-loader --save-dev
# or
yarn add --dev svg-loader
```

## Configuration

```js
// ...
{
  test: /\.svg$/,
  loader: 'svg' // 👈 Add loader
},
// ...
```

## Usage

svg-loader exports an object with two properties:

- `attributes` - the root SVG tag attributes.
- `content` - the SVG content (excluding the root `svg` tag).

See example output for `require('./icon.svg')`:

```js
{
  attributes: {
    xmlns: 'http://www.w3.org/2000/svg',
    viewBox: '0 0 448 512'
  },
  content: '<path d="M441.9 167.3l-19.8-19.8c-4.7-4.7-12.3-4.7-17 0L224 328.2 42.9 147.5c-4.7-4.7-12.3-4.7-17 0L6.1 167.3c-4.7 4.7-4.7 12.3 0 17l209.4 209.4c4.7 4.7 12.3 4.7 17 0l209.4-209.4c4.7-4.7 4.7-12.3 0-17z"/>'
}
```

## License

[MIT © Andrei Terentev](https://opensource.org/licenses/mit-license.php)
