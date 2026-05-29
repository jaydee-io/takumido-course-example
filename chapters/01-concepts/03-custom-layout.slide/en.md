# Beyond primitives: custom layouts

> When the built-in layouts aren't enough, define your own.

::: slot headline

Compose your own layout with the **same DSL** as the primitives.

:::

::: slot detail

The `takumido-*` layouts (text, code, columns, title…) cover the common cases. But a course may need a specific arrangement — a title band above a two-column body, for instance.

Just add a `<id>.layout.yaml` file to the repository's `layouts/` folder. It declares **slots** (typed content regions) and a **composition** (grid, stack or flex). The pipeline exposes it to the renderer exactly like a primitive — no frontend code.

This slide uses the custom `spotlight` layout, defined in `layouts/spotlight.layout.yaml`.

:::

::: slot aside

> The `takumido-` prefix is reserved for platform primitives: a custom layout must pick a different identifier.

:::
