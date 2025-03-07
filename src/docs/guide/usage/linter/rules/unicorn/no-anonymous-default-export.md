<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# unicorn/no-anonymous-default-export <Badge type="info" text="Restriction" />

<div class="rule-meta">
</div>

### What it does

Disallow anonymous functions and classes as the default export

### Why is this bad?

Naming default exports improves codebase searchability by ensuring
consistent identifier use for a module's default export, both where it's
declared and where it's imported.

### Example

Examples of **incorrect** code for this rule:

```javascript
export default class {}
export default function () {}
export default () => {};
module.exports = class {};
module.exports = function () {};
module.exports = () => {};
```

Examples of **correct** code for this rule:

```javascript
export default class Foo {}
export default function foo () {}

const foo = () => {};
export default foo;

module.exports = class Foo {};
module.exports = function foo () {};

const foo = () => {};
module.exports = foo;
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/unicorn/no_anonymous_default_export.rs)
