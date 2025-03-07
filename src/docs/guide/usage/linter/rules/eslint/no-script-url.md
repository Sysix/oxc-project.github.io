<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# eslint/no-script-url <Badge type="info" text="Style" />

<div class="rule-meta">
</div>

### What it does

Disallow javascript: urls

### Why is this bad?

Using `javascript:` URLs is considered by some as a form of `eval`. Code
passed in `javascript:` URLs must be parsed and evaluated by the browser
in the same way that `eval` is processed. This can lead to security and
performance issues.

### Examples

Examples of **incorrect** code for this rule

```javascript
/*eslint no-script-url: "error"*/

location.href = "javascript:void(0)";

location.href = `javascript:void(0)`;
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/eslint/no_script_url.rs)
