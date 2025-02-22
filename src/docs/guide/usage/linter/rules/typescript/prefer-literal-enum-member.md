<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# typescript/prefer-literal-enum-member <Badge type="info" text="Restriction" />

<div class="rule-meta">
</div>

### What it does

Explicit enum value must only be a literal value (string, number, boolean, etc).

### Why is this bad?

TypeScript allows the value of an enum member to be many different kinds of valid JavaScript expressions.
However, because enums create their own scope whereby each enum member becomes a variable in that scope, developers are often surprised at the resultant values.

### Example

```ts
const imOutside = 2;
const b = 2;
enum Foo {
  outer = imOutside,
  a = 1,
  b = a,
  c = b,
}
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/typescript/prefer_literal_enum_member.rs)
