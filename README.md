# Checkpoint

A checkout desk for a classroom equipment room. Scan the gear, scan the badge, and the room
knows who has what — on one Mac, with no account to make and no server to run.

**[Download →](https://github.com/cowfollowdog/checkpoint-releases/releases/latest)**

Checkpoint replaces the paper sign-out sheet. A student walks up with a camera or a tripod,
two scans happen, and the loan is recorded. When the gear comes back, one scan closes it.
Everything else in the app exists to answer the question the sheet could never answer
quickly: *what is still out, and who has it?*

## At the desk

**Start Checkpoint** (`⌘⇧K`) opens the desk in its own window. It keeps a running tally
while it is open and hands back a summary when you end it, so a class period has a
beginning and an end rather than blurring into the next one.

- **Check In and Check Out are two buttons**, always in the same place. The desk never
  guesses what a scan means from what came before it — the mode is something you chose and
  can see.
- **Checking in needs no badge.** Scan the gear and it's back; the loan already knows whose
  it was. Checking out always records a student. If your room wants a name on returns too,
  a setting takes it the other way.
- **Two columns.** What the room is still owed on the left, what has come back on the right,
  newest highlighted. After a return, whoever it belonged to pins to the top — the next
  question is always "what else do they have?"
- **Due dates read in three states**: overdue, due today, and everything else.
- **A second badge mid-checkout is loud** — a banner, a distinct sound, and the header
  redrawing — because silently switching students is how gear goes missing. Switch, ignore,
  or ask, whichever your room prefers.
- **A barcode that won't scan is not a dead end.** Type the tag instead and the confirmation
  offers a *this label needs reprinting* box — the two seconds in which anyone knows the
  label has started to fail.
- **The scanned thing is always named**, by name and tag, in every message and in a
  permanent *Last scanned* line. A refused scan leaves a trace instead of nothing.
- **Undo, not confirmation.** The scan path never stops to ask, so a line of students keeps
  moving; mistakes are corrected after the fact.

## Behind the desk

The main window is the teacher's, and the desk runs independently of it.

- **Dashboard** — what's out now, what's overdue, what just happened.
- **Equipment** — items and categories, with fast entry for a tag you've just scanned and
  never registered.
- **Kits** — a bag that checks out in one scan, and is caught when it comes back short.
- **Students** — the roster, with CSV import. A student can have more than one badge, so a
  replacement card doesn't create a second person.
- **History** — every event, filterable, with corrections on any loan: mark returned,
  backdate to the end of last class, transfer to another student, mark lost, undo a
  mistake. Each correction is recorded with a reason rather than overwriting the original.
- **Labels** — printable asset tags and student badges.
- **Settings** — desk behaviour, due dates, sounds, appearance, and an optional lock on the
  teacher's side using Touch ID or your Mac login password.

## Labels and printing

Labels are Code 128, generated at an exact size. The app pins printing to 100 %, zeroes the
margins, and removes the scaling control from the print dialog, because a label scaled to
97 % looks fine and doesn't scan.

Run the calibration page once per printer (**Labels › Printer alignment**) and every sheet
after that lands where the labels are. If a barcode genuinely won't fit the stock you've
chosen, the app says so and tells you what would fit, rather than shrinking the bars until
they're unreadable.

## Your records

Everything stays on the Mac in a single database file, with timestamped backups taken
automatically — including one before any change to the data format. Restore from a backup
is a button, not a support call. Tables export to CSV.

The record of who had what is append-only: corrections are added on top, so the history
shows what happened *and* what was fixed.

There is no account, no sign-in, and no network call of any kind. Nothing is uploaded, and
the app does not phone home or check for updates.

Checkout logs of student names are best treated as education records — keep exports on the
teacher's side of the room.

## Accessibility

Fully navigable with VoiceOver, including the actions on a history row. Status colours are
always paired with a symbol and a word, both palettes are tested against the window
background rather than judged by eye, and **Increase Contrast** raises them further. The
desk's largest text scales with the system text size.

## Requirements

- macOS 26 or later.
- Apple silicon or Intel.
- Any barcode scanner that types what it reads — USB or Bluetooth, no driver, no setup.
- A printer, if you want to make labels.

## Installing

1. Open the downloaded `.dmg`.
2. Drag **Checkpoint** onto the **Applications** folder beside it.
3. Open it from Applications.

Drag it across rather than running it from the mounted disk image — macOS runs apps
launched from a disk image out of a temporary read-only location, which breaks things
quietly.

The app is signed and notarized, so it opens with a double-click, and it works offline.

## Updating

Quit Checkpoint, open the new `.dmg`, drag it across, and choose **Replace**. Your records
are outside the app and are never touched by an update — deleting the app doesn't remove
them either. The app does not check for new versions, so watch this page if you want to
know one exists.

## Problems

Open an [issue](https://github.com/cowfollowdog/checkpoint-releases/issues). What you
scanned, what you expected, and what happened instead is usually enough.

---

Checkpoint © 2026 Aaron Hua. All rights reserved.
