<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# promise/valid-params <Badge type="info" text="Correctness" />

<div class="rule-meta">
</div>

### What it does

Enforces the proper number of arguments are passed to Promise functions.

### Why is this bad?

Calling a Promise function with the incorrect number of arguments can lead to unexpected
behavior or hard to spot bugs.

### Examples

Examples of **incorrect** code for this rule:

```javascript
Promise.resolve(1, 2);
```

Examples of **correct** code for this rule:

```javascript
Promise.resolve(1);
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/promise/valid_params.rs)
