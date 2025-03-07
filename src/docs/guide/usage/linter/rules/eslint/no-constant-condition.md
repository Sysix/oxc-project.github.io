<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# eslint/no-constant-condition <Badge type="info" text="Correctness" />

<div class="rule-meta">
<Alert class="default-on" type="success">
<span class="emoji">✅</span> This rule is turned on by default.
</Alert>
</div>

### What it does

Disallow constant expressions in conditions

### Why is this bad?

A constant expression (for example, a literal) as a test condition might
be a typo or development trigger for a specific behavior.

This rule disallows constant expressions in the test condition of:

- `if`, `for`, `while`, or `do...while` statement
- `?`: ternary expression

### Example

Examples of **incorrect** code for this rule:

```js
if (false) {
  doSomethingUnfinished();
}

if (new Boolean(x)) {
  doSomethingAlways();
}
if ((x ||= true)) {
  doSomethingAlways();
}

do {
  doSomethingForever();
} while ((x = -1));
```

Examples of **correct** code for this rule:

```js
if (x === 0) {
  doSomething();
}

while (typeof x === "undefined") {
  doSomething();
}
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/eslint/no_constant_condition.rs)
