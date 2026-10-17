---
name: dry-principle
description: Applies the Don't Repeat Yourself principle without over-abstracting. Use when writing or reviewing code that duplicates logic, constants, or config, when deciding whether to extract a shared helper, or when asked to review code for DRY compliance.
---

# DRY Principle

Remove duplication that represents the same knowledge, within the limits of the laws below.

## Iron Laws

1. **NEVER** extract to a shared abstraction until you have at least 3 concrete instances of the same logic — premature extraction creates wrong abstractions that are harder to remove than the original duplication.
2. **ALWAYS** maintain a single source of truth for configuration values — the same constant or config value defined in two places will diverge and cause bugs.
3. **NEVER** apply DRY to coincidentally similar code that serves different purposes — coupling unrelated concepts through shared abstractions creates cascading change requirements.
4. **ALWAYS** prefer readability over DRY when the abstraction requires indirection that obscures what the code does — a small amount of duplication is often better than an obscure helper.
5. **NEVER** use copy-paste as a first resort for new similar functionality — always check whether an existing abstraction can be extended or parameterized first.
6. **NEVER** DRY up test setup at the cost of readability — tests should be self-contained; some duplication in test setup is acceptable.
