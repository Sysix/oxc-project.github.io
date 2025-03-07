<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# typescript/triple-slash-reference <Badge type="info" text="Correctness" />

<div class="rule-meta">
<Alert class="default-on" type="success">
<span class="emoji">✅</span> This rule is turned on by default.
</Alert>
</div>

### What it does

Disallow certain triple slash directives in favor of ES6-style import declarations.

### Why is this bad?

Use of triple-slash reference type directives is generally discouraged in favor of ECMAScript Module imports.

### Example

```ts
/// <reference lib="code" />
globalThis.value;
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/typescript/triple_slash_reference.rs)
