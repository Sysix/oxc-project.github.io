<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# eslint/default-case <Badge type="info" text="Restriction" />

<div class="rule-meta">
</div>

### What it does

Require default cases in switch statements

### Why is this bad?

Some code conventions require that all switch statements have a default case, even if the
default case is empty.

### Example

```javascript
switch (foo) {
  case 1:
    break;
}
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/eslint/default_case.rs)
