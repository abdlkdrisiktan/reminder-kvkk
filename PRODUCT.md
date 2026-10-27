# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

This repository is the public website for an Android app: a bilingual (TR default, EN under `en/`) static landing page plus the privacy policy, terms of use and a 404 page, served from GitHub Pages under `/reminder-kvkk/`. The app itself is not in this repository.

## Users

Primary: people who take medication on a schedule, and the relatives who help them. They use the app on their own Android phone to be reminded at the right time, mark a dose as taken, and know when they are running low.

Older users are part of the audience, so reading comfort and clear controls matter on every surface.

Secondary visitors of this site: Google Play reviewers and anyone checking the privacy policy or KVKK disclosures before installing.

## Product Purpose

Hatırlatıcı rings at the exact scheduled time, even on the lock screen and after a restart, lets the user check a dose off in one tap, tracks remaining stock and shows a 30-day history with an adherence rate. Success is a reminder never missed and a user who trusts the app with their routine.

The website's job: explain what the app does, send visitors to Google Play, and publish the privacy policy and terms the store listing links to.

## Positioning

Reminder data stays on the device: no account, no sign-up, works offline. The app shows Google AdMob ads (banner + rewarded, UMP consent for EEA/UK/CH), so data leaving the phone is Firebase Analytics, Remote Config and AdMob traffic (incl. advertising ID). Reminder content never leaves the device, and every privacy claim must stay consistent with that.

## Operating Context

- Android only, distributed through Google Play (`tr.com.hatirlatici`).
- Relies on notification, exact alarm, full-screen intent and boot-completed permissions; battery optimisation on some phones can delay reminders, and the site says so honestly.
- Legal pages are written for KVKK (Law No. 6698). The Turkish versions prevail; the English pages are translations.
- Developer and data controller: Abdulkadir Işıktan, contact kadirisiktan@gmail.com.

## Capabilities and Constraints

- Features: exact-time alarms, one-tap Taken / Snooze / Undo from the notification, multiple times per day, specific weekdays, duration and meal timing, stock tracking with low-stock alerts, 30-day history with adherence rate, home screen widget.
- Not a medical device and not a substitute for a doctor or pharmacist; the terms carry this notice and new copy must not contradict it or make medical claims.
- Public copy currently uses the neutral name "Hatırlatıcı" and generic "reminder" wording rather than "pill" or "medication", even though the main use is medication.
- Open decision: paid features. The terms say some features (such as the widget or lifting a free-plan limit) may become paid through Google Play; nothing is priced or announced yet.
- The site is plain static HTML/CSS with no build step. Every page must work in both TR and EN, and 404.html uses root-absolute `/reminder-kvkk/` paths.

## Brand Commitments

- Name: Hatırlatıcı.
- `logo.svg` (calendar mark) and the app's teal and amber colours are shared with the app and must not change.
- Voice: plain, warm, second person singular in Turkish ("sen"), short sentences, no hype.

## Evidence on Hand

- Real app screenshots: the owner can supply them on request. The site currently shows a hand-drawn HTML mockup of the Today screen, which should be replaced or checked against real screens.
- No user reviews, ratings, download counts, press or testimonials exist. Do not invent any.

## Product Principles

1. Privacy claims are exact. Say what stays on the device and name what does not (Firebase).
2. Reliability comes before features. Being on time is the promise, and its limits (battery savers, permissions) are stated plainly.
3. Readable for everyone, including older users and people reading while unwell.
4. Bilingual parity. A change in one language ships in the other.
5. No medical claims and no invented proof.

## Accessibility & Inclusion

Target WCAG 2.2 AA at minimum, with older users in mind: body text 17px or larger, strong contrast in light and dark themes, large touch targets, visible keyboard focus, and motion that respects `prefers-reduced-motion`.
