# tailwindcss-grid-system

[![npm version][version-badge]][version]
![Build Status](https://github.com/hamidreza4dev/tailwindcss-grid-system/workflows/publish-package/badge.svg)
[![License: MIT][license-badge]][license]

Bootstrap **v5** flexbox grid system as a Tailwind CSS plugin.

## Installation

```shell
npm i -D tailwindcss-grid-system
```

In `tailwind.config.js` file:

```js
/** @type {import("tailwindcss").Config} */
module.exports = {
  plugins: [
    require('tailwindcss-grid-system'),
  ],
};
```
or `tailwind.config.ts` with typescript:

```js
import { Config } from 'tailwindcss';
export default {
  plugins: [
    require('tailwindcss-grid-system'),
  ],
} satisfies Config
```

And don't forget to include `components` and `utilities` in your tailwind base
css file:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

This will generate Bootstrap v5 flexbox grid.

\* **NOTE**: When using the `.container` class from this plugin you will need to
[disable](https://tailwindcss.com/docs/container#disabling-entirely) the core
[container plugin](https://tailwindcss.com/docs/container/) as both plugins
expose a `.container` class.

## Features & Tailwind CSS options support

- ✅ custom screens
- ✅ custom separator
- ✅ custom prefix
- ✅ important
- ✅ rtl support

## Options

- Original Bootstrap grid's options:

  - `gridColumns` (default - `12`) - grid size
  - `gridGutterWidth` (default - `"1.5rem"`) - container and rows gutter width
  - `gridGutters` (default - `theme.spacing` (default tailwind spacings)) - gutter variable class steps (`--twg-gutter-x`, `--twg-gutter-y`)
  - `containerMaxWidths` (default - `{}`) - the `max-width` container value for each breakpoint

- Extra options:
  - `generateContainer` (default - `true`) - whether to generate `.container` and `.container-fluid` classes
  - `rtl` (default - `false`) - rtl support (`.offset-x` classes will start
    responding to `[dir=ltr]` / `[dir=rtl]`)
  - `respectImportant` (default - `true`) - whether it should respect the `important`
    root config option


## Related

[version-badge]: https://badge.fury.io/js/tailwindcss-grid-system.svg
[version]: https://www.npmjs.com/package/tailwindcss-grid-system
[license-badge]: https://img.shields.io/badge/License-MIT-yellow.svg
[license]: https://opensource.org/licenses/MIT