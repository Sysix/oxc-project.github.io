<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# eslint/no-nonoctal-decimal-escape <Badge type="info" text="Correctness" />

<div class="rule-meta">
<Alert class="default-on" type="success">
<span class="emoji">✅</span> This rule is turned on by default.
</Alert>
<Alert class="fix" type="info">
<span class="emoji">🚧</span> An auto-fix is still under development.
</Alert>
</div>

### What it does

This rule disallows \8 and \9 escape sequences in string literals

### Why is this bad?

ECMAScript specification treats \8 and \9 in string literals as a legacy feature

### Example

```javascript
incorrect: "\8";
("\9");
correct: "8";
("\\9");
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/eslint/no_nonoctal_decimal_escape.rs)
