<!-- emendrix:output-repo b7f4a1c2-9e3d -->
# Regulatory changelogs

What changed in EU legislation, provision by provision, computed rather than summarised.

When a watched act is amended, [emendrix](https://emendrix.eu) fetches both consolidated versions,
computes a structural diff over their provision trees, corroborates it against the Union's own
modification metadata and against the amending act's own instruction prose, and commits the result
here. The browsable form of this data, with the methodology and the measured rates, is at
**<https://emendrix.eu>**.

## Layout

```
<corpus>/<act>/CHANGELOG.md            the human-readable changelog, newest first
<corpus>/<act>/changes/<version>.json  the same events as structured JSON
```

One directory per act, namespaced by the corpus it came from; `eu` is the only one so far. The
JSON carries a `schema_version` and is documented in the
[emendrix repository](https://github.com/emendrix/emendrix).

## How to read it honestly

**A disagreement between the sources is recorded, never resolved away.** A change ships marked
disputed when they disagree about whether or how a provision changed, and it still counts in every
published rate. About half the changes here carry that mark, and the
[methodology page](https://emendrix.eu/methodology/) breaks it into the three shapes it takes and
says what each does and does not mean.

**A change with no text on either side is a finding, not a defect.** It means one source named a
provision that the text comparison found no difference in. It is shown, counted and labelled.

**The dates are the ones the documents state.** Where an act does not say when an amendment
applies, this data says it does not know rather than inferring it.

**Figures move when defects are found.** The corpus is corrected in place as parsing and
corroboration improve, and the published rates move with it, so cite the date you read a figure.

## Licence

Two layers, two holders. The quoted legislative texts are © European Union, reused under
Commission Decision 2011/833/EU, and only the Official Journal is authentic. Everything computed
over them is CC BY 4.0, attributable to emendrix. The detail is in
[`LICENCE-NOTICE.md`](./LICENCE-NOTICE.md) and the full licence text in [`LICENSE`](./LICENSE).

> Not legal advice: this output is machine-computed from published texts, carries no lawyer's
> review, and is engineering assistance only.
