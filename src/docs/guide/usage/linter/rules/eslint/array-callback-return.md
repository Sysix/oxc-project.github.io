<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# eslint/array-callback-return <Badge type="info" text="Pedantic" />

<div class="rule-meta">
</div>

### What it does

Enforce return statements in callbacks of array methods

### Why is this bad?

Array has several methods for filtering, mapping, and folding.
If we forget to write return statement in a callback of those, it’s probably a mistake.
If you don’t want to use a return or don’t need the returned results,
consider using .forEach instead.

### Example

```javascript
let foo = [1, 2, 3, 4];
foo.map((a) => {
  console.log(a);
});
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/eslint/array_callback_return/mod.rs)
