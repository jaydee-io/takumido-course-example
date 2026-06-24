# Versioning and Publishing a Course

> A TakumiDô course is a git repository versioned with semver tags.

::: slot body

The TakumiDô **content pipeline** loads a course by checking out a specific semver tag. This guarantees reproducibility: the version shown to apprentices is always the one recorded when the course was registered.

To publish a new version of a course:

```bash
# 1. Commit local changes
git add .
git commit -m "feat: add chapter 03-navigation"

# 2. Create an annotated semver tag
git tag -a v1.2.0 -m "Add navigation chapter — 3 chapters, 12 slides"

# 3. Push the tag to the remote repository
git push origin v1.2.0
```

The TakumiDô backend resolves the **latest compatible version** (e.g. `^1.0.0`) from the repository's tag list. Once the tag is visible, the new version is available to trainers.

> **Best practice:** use annotated tags (`-a`) rather than lightweight tags — they carry a message and a date, making version auditing straightforward.

:::
