<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# unicorn/prefer-add-event-listener <Badge type="info" text="Suspicious" />

<div class="rule-meta">
<Alert class="fix" type="info">
<span class="emoji">🚧</span> An auto-fix is still under development.
</Alert>
</div>

### What it does

Enforces the use of `.addEventListener()` and `.removeEventListener()` over their `on`-function counterparts.

For example, `foo.addEventListener('click', handler);` is preferred over `foo.onclick = handler;` for HTML DOM Events.

### Why is this bad?

There are [numerous advantages of using `addEventListener`](https://stackoverflow.com/questions/6348494/addeventlistener-vs-onclick/35093997#35093997). Some of these advantages include registering unlimited event handlers and optionally having the event handler invoked only once.

### Examples

Examples of **incorrect** code for this rule:

```javascript
foo.onclick = () => {};
```

Examples of **correct** code for this rule:

```javascript
foo.addEventListener("click", () => {});
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/unicorn/prefer_add_event_listener.rs)
