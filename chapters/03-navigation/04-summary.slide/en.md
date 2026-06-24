# Summary — TakumiDô at a Glance

> All mechanics, all roles.

::: slot left

## What you have seen

**Content & structure**
- Course = git repository, versioned with semver tags
- Chapters, slides, declarative layouts, i18n

**Live session**
- Trainer and Apprentice roles
- Real-time slide synchronization

**Apprentice navigation**
- Play mode (automatic follow) and Pause mode (free browsing)
- High-Water Mark: progressive unlock
- Tree chapter menu
- Universal keyboard shortcuts

**Resilience**
- Automatic reconnection
- Play/Pause posture preserved

:::

::: slot right

## Resources

**Create your own course:**
Clone this repository and adapt the chapters — the TakumiDô pipeline handles the rest.

**Minimal structure:**

```
my-course/
├── course.yaml
├── i18n/en.yaml
└── chapters/
    └── 01-intro/
        ├── chapter.yaml
        └── 01-welcome.slide/
            ├── meta.yaml
            └── en.md
```

**Tag and register:**
```bash
git tag -a v1.0.0 -m "Initial release"
git push origin v1.0.0
```

> **Next step:** submit the repository URL in TakumiDô and launch your first live session.

:::
