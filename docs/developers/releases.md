# Releases

## Parts

Each part repo has a **release** workflow that publishes into the main repo:

- **Nightly** &mdash; every day (only if something changed), as `<part>-nightly`.
- **Stable** &mdash; **Actions → release → Run workflow** and type a version (like `1.2.5`), or push a tag:

```bash
git tag v1.2.5
git push origin v1.2.5
```

It's published as `<part>-v1.2.5`.

### needs.txt

If a part needs a minimum version of another part, add `needs.txt` to its repo, one per line:

```
streamer v1.4
```

Updates are held back ("Waiting") until that's met.

## Core

```bash
git push origin nightly:builds
git tag core-v1.2.5
git push origin core-v1.2.5
```

The **core release** workflow makes the `core-v1.2.5` release.

## AI models

`export.py --release` in the AI repo publishes `ai-<kind>-vX` and starts the **ai stats** workflow, which tests the models and adds a **Model check** section to the release notes.

## updates.txt

The **updates list** workflow rebuilds `updates.txt` from all releases whenever one is published, and uploads it to the `updates` release. Printer Buddy reads it to know what's newest.
