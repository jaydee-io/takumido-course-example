# Reconnection — Session Resilience

> A network drop does not lose your place.

::: slot headline

TakumiDô preserves the apprentice's **Play/Pause posture** across network interruptions.

:::

::: slot detail

When the WebSocket connection is interrupted (Wi-Fi loss, device sleep, network switch), the apprentice enters the **Disconnected** state. A visual indicator signals the disconnection.

On reconnection, the server restores the full state:

- **Posture preserved:** if the apprentice was in **Play**, they resume in Play; if they were in **Pause**, they resume in Pause at the same slide.
- **HWM synced:** the High-Water Mark is updated with the server's current value, which may unlock new slides if the trainer advanced during the disconnection.
- **Slide synced:** in Play mode, the apprentice automatically returns to the trainer's current slide.

Reconnection is automatic — no action required from the apprentice.

:::

::: slot aside

**State machine:**

`Play` → `Disconnected` → `Play` ✓

`Pause` → `Disconnected` → `Pause` ✓ (same slide)

:::
