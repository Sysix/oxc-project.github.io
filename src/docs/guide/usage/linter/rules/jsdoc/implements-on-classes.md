<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# jsdoc/implements-on-classes <Badge type="info" text="Correctness" />

<div class="rule-meta">
</div>

### What it does

Reports an issue with any non-constructor function using `@implements`.

### Why is this bad?

Constructor functions should be
whether marked with `@class`, `@constructs`, or being an ES6 class constructor.

### Examples

Examples of **incorrect** code for this rule:

```javascript
/**
 * @implements {SomeClass}
 */
function quux() {}
```

Examples of **correct** code for this rule:

```javascript
class Foo {
  /**
   * @implements {SomeClass}
   */
  constructor() {}
}
/**
 * @implements {SomeClass}
 * @class
 */
function quux() {}
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/jsdoc/implements_on_classes.rs)
