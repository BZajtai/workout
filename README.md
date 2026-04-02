# Gym Tracker

A personal workout tracking app built as a single self-contained HTML file, designed to run on iPhone via Safari and be saved to the home screen as a web app.

## Features

- **Free-form session logging** — pick any exercises from your list each session
- **Four exercise types** with appropriate inputs:
  - Standard — sets, reps, and optional weight (kg)
  - Count — sets and reps, no weight (e.g. pushups, squats)
  - Timed — duration only (e.g. plank)
  - Class — no inputs, just records that the session happened (e.g. pilates, swimming)
- **Per-exercise history** — last session's numbers shown at a glance, with expandable older history
- **Same-day session merging** — saving a second time on the same day adds to the existing session rather than overwriting; weighted exercises accumulate, count/timed/class exercises are kept as separate entries
- **Calendar tab** — monthly view showing which days you worked out, scrollable by month, with a running streak counter
- **Session history tab** — expandable cards showing every past session
- **JSON backup** — export and import your full history at any time


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
| `"timed"` | duration | holds and timed exercises |
| `"class"` | none | pilates, swimming, yoga, or any class-based session |

Any exercise in the `Cardio` category automatically gets the timed input regardless of whether `type` is set.

## Calendar auto-marking

A day is automatically marked on the calendar when a saved session meets either of these conditions:

- At least one `class` type exercise was logged
- At least 3 non-class exercises were logged

Days that don't meet the threshold can be marked manually by tapping them. Tap again to unmark. Long-pressing a day that has a saved session opens a summary of what was logged.

## Icon credits

<a href="https://www.flaticon.com/free-icons/pec" title="pec icons">Pec icons created by Fahrul Oktaviana - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/rowing-pull" title="rowing pull icons">Rowing pull icons created by kerismaker - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/chest-press" title="chest press icons">Chest press icons created by kmg design - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/strength" title="strength icons">Strength icons created by gravisio - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/leg-press" title="leg press icons">Leg press icons created by agus raharjo - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/triceps" title="triceps icons">Triceps icons created by Freepik - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/chest-press" title="chest-press icons">Chest-press icons created by kmg design - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/push-ups" title="push ups icons">Push ups icons created by justicon - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/lat-pulldown" title="lat pulldown icons">Lat pulldown icons created by Freepik - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/pec" title="pec icons">Pec icons created by Fahrul Oktaviana - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/rowing-machine" title="rowing machine icons">Rowing machine icons created by kerismaker - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/muscle" title="muscle icons">Muscle icons created by justicon - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/lunges" title="lunges icons">Lunges icons created by Flat Icons - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/barbell" title="barbell icons">Barbell icons created by gravisio - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/plank" title="plank icons">Plank icons created by Freepik - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/elliptical" title="elliptical icons">Elliptical icons created by Flat Icons - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/workout" title="workout icons">Workout icons created by ultimatearm - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/swimming" title="swimming icons">Swimming icons created by Chattapat - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/pilates" title="pilates icons">Pilates icons created by Freepik - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/exercise" title="exercise icons">Exercise icons created by ultimatearm - Flaticon</a>

<a href="https://www.flaticon.com/free-icons/pilates" title="pilates icons">Pilates icons created by photo3idea_studio - Flaticon</a>
