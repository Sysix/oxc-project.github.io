<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# eslint/no-template-curly-in-string <Badge type="info" text="Style" />

<div class="rule-meta">
<Alert class="fix" type="info">
<span class="emoji">🚧</span> An auto-fix is still under development.
</Alert>
</div>

### What it does

Disallow template literal placeholder syntax in regular strings

### Why is this bad?

ECMAScript 6 allows programmers to create strings containing variable or
expressions using template literals, instead of string concatenation, by
writing expressions like `${variable}` between two backtick quotes. It
can be easy to use the wrong quotes when wanting to use template
literals, by writing `"${variable}"`, and end up with the literal value
`"${variable}"` instead of a string containing the value of the injected
expressions.

### Example

Examples of **incorrect** code for this rule:

```javascript
/*eslint no-template-curly-in-string: "error"*/
"Hello ${name}!";
"Hello ${name}!";
"Time: ${12 * 60 * 60 * 1000}";
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/eslint/no_template_curly_in_string.rs)
