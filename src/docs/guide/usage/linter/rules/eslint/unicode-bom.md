<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# eslint/unicode-bom <Badge type="info" text="Restriction" />

<div class="rule-meta">
<Alert class="fix" type="info">
<span class="emoji">🛠️</span> An auto-fix is available for this rule.
</Alert>
</div>

### What it does

Require or disallow Unicode byte order mark (BOM)

### Why is this bad?

The Unicode Byte Order Mark (BOM) is used to specify whether code units are big endian or
little endian. That is, whether the most significant or least significant bytes come first.
UTF-8 does not require a BOM because byte ordering does not matter when characters are a
single byte. Since UTF-8 is the dominant encoding of the web, we make "never" the default
option.

### Example

```javascript
var a = 123;
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/eslint/unicode_bom.rs)
