# Today I Learned

> So you don't have to.

A small collection of write-ups for patterns, recipes, and gotchas worth
remembering — captured once, plainly, so the next person (often future-me)
can skip the part where I learned it the hard way.

Each entry stands on its own. No required reading order. Project-specific
identifiers are scrubbed; the shape of each pattern is what's portable.

## Index

- [**Shipping iOS to TestFlight from GitHub Actions**](./github-to-testflight.md) —
  an opinionated, solo-developer-friendly pattern for `git push main` → signed
  TestFlight build, no local Mac required for the build itself. **Part 1** is
  the foundational pipeline: the two-repo split for signing material, Fastlane
  Match, the deploy / bootstrap / credential-check workflows, the Xcode build
  settings that aren't optional, and the real errors you'll hit on the way
  through. **Part 2** is an optional cost-cutting layer: route CI to your own
  Mac when it's available and fall back to GitHub-hosted automatically when
  it isn't, via a tiny preflight chooser job. A sidebar in Part 1 also covers
  a structured PR-failure-comment shape that lets a CI bot or LLM agent read
  test failures from the GitHub API without anyone copy-pasting from the
  Actions UI.

## License

[MIT](./LICENSE). Use any of this, adapt it, ship it.
