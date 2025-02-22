<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# jest/require-to-throw-message <Badge type="info" text="Correctness" />

<div class="rule-meta">
</div>

### What it does

This rule triggers a warning if `toThrow()` or `toThrowError()` is used without an error message.

### Example

```javascript
// invalid
test("all the things", async () => {
  expect(() => a()).toThrow();
  expect(() => a()).toThrowError();
  await expect(a()).rejects.toThrow();
  await expect(a()).rejects.toThrowError();
});

// valid
test("all the things", async () => {
  expect(() => a()).toThrow("a");
  expect(() => a()).toThrowError("a");
  await expect(a()).rejects.toThrow("a");
  await expect(a()).rejects.toThrowError("a");
});
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/jest/require_to_throw_message.rs)
