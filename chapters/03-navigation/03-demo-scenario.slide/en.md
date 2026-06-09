# Full Demo Scenario

> Reproduce every state-machine transition in a single demo.

::: slot headline

This scenario covers: **Play → Pause** (shortcut, rewind, menu click) · **Pause → Play** (resync) · **HWM** · **reconnection**.

:::

::: slot detail

**Prerequisites:** two browsers open on the same session — one as Trainer, one as Apprentice.

**Steps:**

1. **Default Play** — Join the session. The apprentice starts in Play mode and automatically follows the trainer.

2. **Play → Pause via `P` shortcut** — Trainer on slide 3. Apprentice presses `P` → FollowIndicator turns CYAN (Pause). Presses `P` again → FollowIndicator GREEN (Play, resynced).

3. **Play → Pause via rewind** — Trainer on slide 5. Apprentice presses `←` → Pause, moves back to slide 4. FollowIndicator CYAN.

4. **Play → Pause via menu click** — Apprentice presses `Space` (resync → Play). Then opens the ChapterMenu and clicks slide 2 → triggers Pause from Play state. Slide 2 is displayed.

5. **HWM unlock** — Trainer advances from slide 5 to 7. In the apprentice's menu, slides 6 and 7 unlock in real time (🔒 badges disappear without reloading).

6. **Resync (Pause → Play)** — Apprentice presses `Space` → FollowIndicator GREEN, jumps back to slide 7 (trainer's position).

7. **Reconnection** — Disable then re-enable the apprentice's Wi-Fi. After reconnection, the apprentice resumes in Play on the trainer's current slide, HWM up to date.

:::

::: slot aside

**Transitions covered:**

- Play → Pause ✓  
  via `←`, via `P`, via menu click
- Pause → Play (resync) ✓  
  via `Space` / `P`
- Menu navigation (HWM-aware) ✓
- Progressive HWM unlock ✓
- Disconnected → Play ✓

:::
