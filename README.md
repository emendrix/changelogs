<!-- emendrix:output-repo b7f4a1c2-9e3d -->
# Regulatory changelogs

Written by emendrix, a regulatory change engine: it watches published legislation, computes a provision-level structural diff when an act is amended, and commits the result here.

Layout — one directory per act, namespaced by the corpus it came from:

```
<corpus>/<act>/CHANGELOG.md          the human-readable changelog, newest first
<corpus>/<act>/changes/<version>.json  the same events as structured JSON
```

The JSON schema is versioned and documented in the emendrix repository. This repository belongs to you: emendrix commits into it and never pushes it anywhere.

> Not legal advice: this output is machine-computed from published texts, carries no lawyer's
> review, and is engineering assistance only.
