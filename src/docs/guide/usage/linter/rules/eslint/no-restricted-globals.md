<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# eslint/no-restricted-globals <Badge type="info" text="Restriction" />

<div class="rule-meta">
</div>

### What it does

This rule allows you to specify global variable names that you don't want to use in your application.

### Why is this bad?

Disallowing usage of specific global variables can be useful if you want to allow a set of global
variables by enabling an environment, but still want to disallow some of those.

For instance, early Internet Explorer versions exposed the current DOM event as a global variable
`event`, but using this variable has been considered as a bad practice for a long time. Restricting
this will make sure this variable isn't used in browser code.

### Example

If we have options:

```json
"no-restricted-globals": ["error", "event"]
```

The following patterns are considered problems:

```javascript
function onClick() {
  console.log(event); // Unexpected global variable 'event'. Use local parameter instead.
}
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/eslint/no_restricted_globals.rs)
