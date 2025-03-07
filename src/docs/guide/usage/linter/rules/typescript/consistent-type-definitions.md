<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# typescript/consistent-type-definitions <Badge type="info" text="Style" />

<div class="rule-meta">
<Alert class="fix" type="info">
<span class="emoji">🛠️</span> An auto-fix is available for this rule.
</Alert>
</div>

### What it does

Enforce type definitions to consistently use either interface or type.

### Why is this bad?

TypeScript provides two common ways to define an object type: interface and type.
The two are generally very similar, and can often be used interchangeably.
Using the same type declaration style consistently helps with code readability.

### Example

```ts
// incorrect, when set to "interface"
type T = { x: number };

// incorrect when set to "type"
interface T {
  x: number;
}
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/typescript/consistent_type_definitions.rs)
