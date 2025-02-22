<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# eslint/no-case-declarations <Badge type="info" text="Pedantic" />

<div class="rule-meta">
</div>

### What it does

Disallow lexical declarations in case clauses.

### Why is this bad?

The reason is that the lexical declaration is visible
in the entire switch block but it only gets initialized when it is assigned,
which will only happen if the case where it is defined is reached.

### Example

```javascript
switch (foo) {
  case 1:
    let x = 1;
    break;
  case 2:
    const y = 2;
    break;
  case 3:
    function f() {}
    break;
  default:
    class C {}
}
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/eslint/no_case_declarations.rs)
