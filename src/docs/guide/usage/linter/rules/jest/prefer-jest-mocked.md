<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# jest/prefer-jest-mocked <Badge type="info" text="Style" />

<div class="rule-meta">
<Alert class="fix" type="info">
<span class="emoji">🛠️</span> An auto-fix is available for this rule for some violations.
</Alert>
</div>

### What it does

When working with mocks of functions using Jest, it's recommended to use the
`jest.mocked()` helper function to properly type the mocked functions. This rule
enforces the use of `jest.mocked()` for better type safety and readability.

Restricted types:

- `jest.Mock`
- `jest.MockedFunction`
- `jest.MockedClass`
- `jest.MockedObject`

### Examples

```typescript
// invalid
(foo as jest.Mock).mockReturnValue(1);
const mock = (foo as jest.Mock).mockReturnValue(1);
(foo as unknown as jest.Mock).mockReturnValue(1);
(Obj.foo as jest.Mock).mockReturnValue(1);
([].foo as jest.Mock).mockReturnValue(1);

// valid
jest.mocked(foo).mockReturnValue(1);
const mock = jest.mocked(foo).mockReturnValue(1);
jest.mocked(Obj.foo).mockReturnValue(1);
jest.mocked([].foo).mockReturnValue(1);
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/jest/prefer_jest_mocked.rs)
