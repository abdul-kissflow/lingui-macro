[![License][badge-license]][license]
[![Version][badge-version]][package]
[![Downloads][badge-downloads]][package]
[![Babel Macro][badge-macro]][linguijs]

# lingui-macro

> [Babel Macros](https://github.com/kentcdodds/babel-plugin-macros) which
> transforms tagged template literals and JSX components to ICU MessageFormat.

`lingui-macro` is modified version of [`@lingui/macro`][linguimacro]
in which `defineMessage` macro returns string instead of MessageDescriptor. (Migration purpose)

## Installation

```sh
npm install --save-dev @lingui/macro@npm:lingui-macro
# yarn add --dev @lingui/macro@npm:lingui-macro
```

## Usage

See the [reference][reference] documentation.

```js
import { setupI18n } from "@lingui/core"
import { defineMessage } from "@lingui/macro"

const message = defineMessage`Hello, my name is {name}`;
// line above is transformed using babel-plugin-macros to this string instead of MessageDescriptor
// const message = `Hello, my name is {name}`;

const i18n = setupI18n();

const message = i18n._(label, {name: "Steve"})
```

## License

[MIT][license]

[license]: https://github.com/abdul-kissflow/lingui-macro/blob/main/LICENSE
[linguijs]: https://github.com/lingui/js-lingui
[reference]: https://lingui.dev/ref/macro/
[linguimacro]: https://www.npmjs.com/package/@lingui/macro
[package]: https://www.npmjs.com/package/lingui-macro
[badge-downloads]: https://img.shields.io/npm/dw/lingui-macro.svg
[badge-version]: https://img.shields.io/npm/v/lingui-macro.svg
[badge-license]: https://img.shields.io/npm/l/lingui-macro.svg
[badge-macro]: https://img.shields.io/badge/babel--macro-%F0%9F%8E%A3-f5da55.svg
