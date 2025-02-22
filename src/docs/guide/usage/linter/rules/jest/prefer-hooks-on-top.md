<!-- This file is auto-generated by tasks/website/src/linter/rules/doc_page.rs. Do not edit it manually. -->

# jest/prefer-hooks-on-top <Badge type="info" text="Style" />

<div class="rule-meta">
</div>

### What it does

While hooks can be setup anywhere in a test file, they are always called in a
specific order, which means it can be confusing if they're intermixed with test
cases.

### Example

```javascript
// invalid
describe("foo", () => {
  beforeEach(() => {
    seedMyDatabase();
  });

  it("accepts this input", () => {
    // ...
  });

  beforeAll(() => {
    createMyDatabase();
  });

  it("returns that value", () => {
    // ...
  });

  describe("when the database has specific values", () => {
    const specificValue = "...";
    beforeEach(() => {
      seedMyDatabase(specificValue);
    });

    it("accepts that input", () => {
      // ...
    });

    it("throws an error", () => {
      // ...
    });

    afterEach(() => {
      clearLogger();
    });

    beforeEach(() => {
      mockLogger();
    });

    it("logs a message", () => {
      // ...
    });
  });

  afterAll(() => {
    removeMyDatabase();
  });
});

// valid
describe("foo", () => {
  beforeAll(() => {
    createMyDatabase();
  });

  beforeEach(() => {
    seedMyDatabase();
  });

  afterAll(() => {
    clearMyDatabase();
  });

  it("accepts this input", () => {
    // ...
  });

  it("returns that value", () => {
    // ...
  });

  describe("when the database has specific values", () => {
    const specificValue = "...";

    beforeEach(() => {
      seedMyDatabase(specificValue);
    });

    beforeEach(() => {
      mockLogger();
    });

    afterEach(() => {
      clearLogger();
    });

    it("accepts that input", () => {
      // ...
    });

    it("throws an error", () => {
      // ...
    });

    it("logs a message", () => {
      // ...
    });
  });
});
```

## References

- [Rule Source](https://github.com/oxc-project/oxc/blob/36ebb3e7841818c238c44349d6cf859db4177d55/crates/oxc_linter/src/rules/jest/prefer_hooks_on_top.rs)
