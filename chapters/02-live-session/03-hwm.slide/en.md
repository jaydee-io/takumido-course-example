# The High-Water Mark

> A progressive lock that unlocks slides at the trainer's pace.

::: slot left

The **High-Water Mark (HWM)** is the index of the furthest slide the trainer has presented during a session. It moves forward as the trainer advances — it never goes back.

Every time the trainer moves to a new slide, the HWM is updated and broadcast to all connected apprentices.

**Locking rule:**
- Slides with index ≤ HWM are **unlocked** — the apprentice can browse them freely.
- Slides with index > HWM are **locked** — they appear greyed out in the chapter menu and cannot be selected.

:::

::: slot right

**Demo scenario:**

Imagine a session with 12 slides. The trainer is on slide 7; the HWM is therefore 7.

| Slide | State |
|-------|-------|
| 1 – 7 | Unlocked |
| 8 – 12 | Locked 🔒 |

When the trainer moves to slide 8, the HWM moves to 8 and slide 8 instantly unlocks for all apprentices.

> **Pedagogical intent:** the apprentice cannot skip ahead. They can, however, review everything already covered.

:::
