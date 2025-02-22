<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# jsdoc/empty-tags <Badge type="info" text="Restriction" />

<div class="rule-meta">
</div>

### What it does

Expects the following tags to be empty of any content:

- `@abstract`
- `@async`
- `@generator`
- `@global`
- `@hideconstructor`
- `@ignore`
- `@inner`
- `@instance`
- `@override`
- `@readonly`
- `@inheritDoc`
- `@internal`
- `@overload`
- `@package`
- `@private`
- `@protected`
- `@public`
- `@static`

### Why is this bad?

The void tags should be empty.

### Examples

Examples of **incorrect** code for this rule:

```javascript
/** @async foo */

/** @private bar */
```

Examples of **correct** code for this rule:

```javascript
/** @async */

/** @private */
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/jsdoc/empty_tags.rs)
