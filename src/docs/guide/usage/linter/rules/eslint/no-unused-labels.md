<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# eslint/no-unused-labels <Badge type="info" text="Correctness" />

<div class="rule-meta">
<Alert class="default-on" type="success">
<span class="emoji">✅</span> This rule is turned on by default.
</Alert>
<Alert class="fix" type="info">
<span class="emoji">🛠️</span> An auto-fix is available for this rule.
</Alert>
</div>

### What it does

Disallow unused labels

### Why is this bad?

Labels that are declared and not used anywhere in the code are most likely an error due to incomplete refactoring.

### Example

```javascript
OUTER_LOOP: for (const student of students) {
  if (checkScores(student.scores)) {
    continue;
  }
  doSomething(student);
}
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/eslint/no_unused_labels.rs)
