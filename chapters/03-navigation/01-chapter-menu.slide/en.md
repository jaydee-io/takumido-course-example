# The Chapter Menu

> The apprentice's free-navigation tool, HWM-aware.

::: slot left

The **chapter menu** is a tree panel displayed in the apprentice view. It lists all chapters and their slides, organized hierarchically.

**Behaviour relative to HWM:**

- Unlocked slides (index ≤ HWM) are **clickable**: the apprentice can navigate to them directly. Clicking a slide behind the current position automatically triggers **Pause** mode.
- Locked slides (index > HWM) are **greyed out** with a lock badge: they cannot be selected.

As the trainer advances, lock badges disappear and new slides become accessible — without reloading the page.

:::

::: slot right

**Typical navigation flow:**

1. Trainer is on slide 5/12, HWM = 5.
2. Apprentice opens the menu → sees 5 accessible slides, 7 locked.
3. Apprentice clicks slide 3 → enters **Pause**, displays slide 3.
4. Trainer moves to 6 → slide 6 unlocks in real time in the menu.
5. Apprentice presses **Space** → returns to **Play**, jumps back to slide 6.

> The chapter menu is available in both Play **and** Pause modes — the apprentice can always see where they stand relative to the trainer.

:::
