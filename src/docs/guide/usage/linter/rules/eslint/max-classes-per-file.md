<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# eslint/max-classes-per-file <Badge type="info" text="Pedantic" />

<div class="rule-meta">
</div>

### What it does

Enforce a maximum number of classes per file

### Why is this bad?

Files containing multiple classes can often result in a less navigable and poorly
structured codebase. Best practice is to keep each file limited to a single responsibility.

### Example

```javascript
class Foo {}
class Bar {}
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/eslint/max_classes_per_file.rs)
