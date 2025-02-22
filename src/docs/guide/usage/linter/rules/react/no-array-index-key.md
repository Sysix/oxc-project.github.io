<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# react/no-array-index-key <Badge type="info" text="Perf" />

<div class="rule-meta">
</div>

### What it does

Warn if an element uses an Array index in its key.

### Why is this bad?

It's a bad idea to use the array index since it doesn't uniquely identify your elements.
In cases where the array is sorted or an element is added to the beginning of the array,
the index will be changed even though the element representing that index may be the same.
This results in unnecessary renders.

### Examples

Examples of **incorrect** code for this rule:

```jsx
things.map((thing, index) => <Hello key={index} />);
```

Examples of **correct** code for this rule:

```jsx
things.map((thing, index) => <Hello key={thing.id} />);
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/react/no_array_index_key.rs)
