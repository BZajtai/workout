# Gym Tracker

A personal workout tracking app built as a single self-contained HTML file.

## Features

- **Free-form session logging** — pick any exercises from your list each session
- **Three exercise types** with appropriate inputs:
  - Standard — sets, reps, and optional weight (kg)
  - Count — sets and reps, no weight (e.g. pushups, squats)
  - Timed — duration only (e.g. plank)
- **Per-exercise history** — last session's numbers shown at a glance, with expandable older history
- **Same-day session merging** — saving a second time on the same day adds to the existing session rather than overwriting; weighted exercises accumulate, count/timed exercises are kept as separate entries
- **Session history tab** — expandable cards showing every past session
- **JSON backup** — export and import your manual history backups

## Customising exercises

The exercise list lives in a clearly marked `CONFIGURATION` block near the top of the `<script>` section in `gym-tracker.html`. Each entry follows this shape:

```js
{ id: "unique_id", name: "Display Name", category: "Category", icon: "icons/filename.png" }
```

The `type` field is optional and controls the input layout:

| type | inputs shown | use for |
|---|---|---|
| *(omitted)* | sets, reps, weight | weighted machines and free weights |
| `"count"` | sets, reps | bodyweight exercises |
| `"timed"` | duration | holds and cardio |

Any exercise in the `Cardio` category automatically gets the timed input regardless of whether `type` is set.
