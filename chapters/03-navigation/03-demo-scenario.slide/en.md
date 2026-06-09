# Full Demo Scenario

> Reproduce every state-machine transition in a single demo.

::: slot headline

This scenario covers: **Play → Pause → rewind → menu → HWM → reconnection → resync**.

:::

::: slot detail

**Prerequisites:** two browsers open on the same session — one as Trainer, one as Apprentice.

**Steps:**

1. **Default Play** — Join the session. The apprentice starts in Play mode and automatically follows the trainer.

2. **Pause via rewind** — Trainer on slide 5. Apprentice presses `←` → enters Pause, moves back to slide 4. The follow indicator turns orange.

3. **Menu navigation** — Apprentice opens the chapter menu → clicks slide 2. Slide 2 is displayed; slides 6+ are greyed out.

4. **HWM unlock** — Trainer advances from slide 5 to 7. In the apprentice's menu, slides 6 and 7 unlock in real time.

5. **Resync** — Apprentice presses `Space` → returns to Play, jumps back to slide 7 (trainer's position).

6. **Reconnection** — Disable then re-enable the apprentice's Wi-Fi. After reconnection, the apprentice resumes in Play on the trainer's current slide, HWM up to date.

:::

::: slot aside

**Transitions covered:**

- Play → Pause ✓
- Pause → Play (resync) ✓
- Menu navigation (HWM-aware) ✓
- Progressive HWM unlock ✓
- Disconnected → Play ✓

:::
