<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# oxc/uninvoked-array-callback <Badge type="info" text="Correctness" />

<div class="rule-meta">
<Alert class="default-on" type="success">
<span class="emoji">✅</span> This rule is turned on by default.
</Alert>
</div>

### What it does

This rule applies when an Array function has a callback argument used for an array with empty slots.

### Why is this bad?

When the Array constructor is called with a single number argument, an array with the specified number of empty slots (not actual undefined values) is constructed.
If a callback function is passed to the function of this array, the callback function is never invoked because the array has no actual elements.

### Example

```javascript
const list = new Array(5).map((_) => createElement());
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/oxc/uninvoked_array_callback.rs)
