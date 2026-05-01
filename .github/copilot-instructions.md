# provision Library — Copilot Instructions

## Deployment model
- This library is consumed as a dependency by projects in the `mydev-online` organization via `deps/provision/`.
- **Any change to this repo must be pushed to GitHub** before rebuilding the consumer project, otherwise the `deps/` copy will revert on next update.

## MJS (Mongoose JS) constraints
- No `let` inside `for..in` loops
- No `try/catch`
- No `Array.forEach`
- No duplicate FFI declarations — declare each FFI function only once
- Heap is ~32KB — avoid large strings and deeply nested objects

## Canon rules
- Do not add extra actions beyond what is explicitly requested.
