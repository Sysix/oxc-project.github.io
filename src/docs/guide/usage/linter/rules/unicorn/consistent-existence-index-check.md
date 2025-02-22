<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# unicorn/consistent-existence-index-check <Badge type="info" text="Style" />

<div class="rule-meta">
<Alert class="fix" type="info">
<span class="emoji">🛠️</span> An auto-fix is available for this rule.
</Alert>
</div>

### What it does

Enforce consistent style for element existence checks with `indexOf()`, `lastIndexOf()`, `findIndex()`, and `findLastIndex()`

### Why is this bad?

This rule is only meant to enforce a specific style and make comparisons more clear.

### Examples

Examples of **incorrect** code for this rule:

```javascript
const index = foo.indexOf("bar");
if (index < 0) {
}
```

```javascript
const index = foo.indexOf("bar");
if (index >= 0) {
}
```

Examples of **correct** code for this rule:

```javascript
const index = foo.indexOf("bar");
if (index === -1) {
}
```

```javascript
const index = foo.indexOf("bar");
if (index !== -1) {
}
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/unicorn/consistent_existence_index_check.rs)
