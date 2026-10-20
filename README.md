# Surgical Pathway — Personal Surgical Productivity

A mobile-first, static, bilingual Arabic/English surgical case log that produces copy-ready monthly productivity fields matching the supplied Google Form screenshot headings.

## Features
- Record **elective**, **emergency**, and **minor clinic** cases.
- Record **completed** versus **planned** operations; only completed procedures count toward monthly totals and weighted surgical points.
- Set surgeon, procedure, date, pseudonymous case code, and locally approved weighting (1–4). Minor clinic fixed at 1; emergency limited to 3–4.
- Monthly report totals and per-surgeon / per-procedure grouped details, with **one copy button per textual Google Forms answer**.
- Extra values for weekly elective OR utilization, on-call days, weekly clinics, vacation days/weeks, and narrative notes.
- Optional monthly target adjusted by 8 points per approved leave week. No unapproved days-to-weeks conversion is inferred.
- JSON backup / restore, CSV export, print-friendly report and mobile-first web app.

## Deploying via GitHub Pages
1. Create a **public repository** on GitHub (e.g. `surgical-productivity`) and upload `index.html` to the repository root.
2. Open **Settings → Pages**, select **Deploy from a branch**, set **Branch = main**, **Folder = /(root)**, then Save.
3. The site is usually available at `https://USERNAME.github.io/surgical-productivity/` after deployment.

These files can alternatively be placed in a subdirectory of an existing GitHub Pages site without altering its root page, subject to its publishing setup.

## Confidentiality and scope
- GitHub Pages **hosts public code** only, not the logged cases.
- Case records and settings are persisted using this browser/device's `localStorage`. This is **not a secure medical record system**, has no login or sync, and can be cleared by browser actions or device failure. Export backups regularly.
- **Never enter real patient names, MRNs, national IDs, or identifiable patient clinical information.** Use pseudonymous local case identifiers instead.
- Upload fields in the source Google Form require manual attachment of authorized system reports; a copy button cannot paste a file into Google Forms.
- No direct authentication, submission to Google Forms, or integration with the hospital information system exists.
- Weighting must be validated against institutional policy and entered by the operator; the app does not infer points from procedure names.