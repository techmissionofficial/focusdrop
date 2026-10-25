# FocusDrop — Scope Plan (written before coding)

## 1. The one thing it does

Turn a named intention into a tracked 25-minute focus session and leave a
clean, persistent daily log behind.

## 2. Inputs / outputs

- Input: a free-text task name.
- Process: a 25-minute countdown (1s ticks).
- Output: a persistent per-day session log with per-session status and
  minutes, plus a daily summary of completed sessions and focused minutes.

## 3. Acceptance criteria (tested)

- [x] Start button stays disabled until a task name is entered.
- [x] Countdown displays mm:ss and reaches 00:00 exactly after 25 minutes.
- [x] On completion, the session is added to the log with today's date.
- [x] "Finish early" logs partial minutes only if time actually passed.
- [x] "Drop session" logs nothing.
- [x] Log survives a page refresh (localStorage).
- [x] No external dependencies; single file runs offline.

## 4. Explicitly out of scope

Accounts, sync, notifications, settings, sounds, mobile app.

## 5. Build notes

Single-page, no frameworks. Plain functions, no build step. XSS-safe log
rendering (escaped).
