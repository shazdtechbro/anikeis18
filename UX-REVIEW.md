# Gift experience review

## Evidence and scope

Reviewed the implemented experience and tested it in Chromium at 375, 768 and 1440 pixels. Attempts to consult the Nielsen Norman Group progressive disclosure article and W3C ARIA modal dialog pattern were blocked with HTTP 403 by the network proxy. No external research or participant usability study was completed.

## Corrections

- Removed kiss spoilers from the box labels and introductory copy.
- Added a confirmation dialog before the irreversible pick. Initial focus goes to the option to return to choosing; cancelling saves nothing.
- Separated the reveal into three user-controlled steps: gift, personal note, final affectionate surprise. No forced countdown or automatic reveal.
- Persisted reveal progress alongside the original gift, so refreshing does not reroll or require repeating completed steps.
- Showed the screenshot reminder and complete receipt after the final reveal.
- Preserved existing completed gift records, including their receipt codes.
- Used browser Web Locks when available to serialize selection across tabs, and storage events to update other open tabs.
- Kept keyboard-accessible controls, a status announcement, visible focus, responsive layouts and reduced-motion support.

## Validation

Verified cancellation does not commit, confirmation saves a pick, early stages do not reveal the kiss, refresh restores the current stage, the final stage exposes the complete receipt, and all three viewport sizes avoid horizontal overflow.

## Remaining limits

The entrance puzzle and gift persistence are client-side. Clearing storage or switching browser/device bypasses the one-pick restriction. A server-side identity and immutable gift record would be needed for enforcement across devices. No such backend is claimed here.
