<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset=".github/brand/banner-dark.svg">
  <img src=".github/brand/banner-light.svg" width="100%" alt="Daily Dispatch: A small SMS service that texts you what you need to hear.">
</picture>

<img src="https://img.shields.io/badge/status-in%20progress-D4845A?style=for-the-badge&labelColor=2A1A0E&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iI0M0NjM3QSIgZD0iTTEyIDFsMi42IDguNEwyMyAxMmwtOC40IDIuNkwxMiAyM2wtMi42LTguNEwxIDEybDguNC0yLjZ6Ii8+PC9zdmc+" alt="Status: in progress">

<img src="https://img.shields.io/badge/Python-2A1A0E?style=for-the-badge&logo=python&logoColor=FFD43B" alt="Python">
<img src="https://img.shields.io/badge/Twilio-2A1A0E?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iMTAiIGZpbGw9Im5vbmUiIHN0cm9rZT0iI0YyMkY0NiIgc3Ryb2tlLXdpZHRoPSIyLjQiLz48Y2lyY2xlIGN4PSI5IiBjeT0iOSIgcj0iMi4xIiBmaWxsPSIjRjIyRjQ2Ii8+PGNpcmNsZSBjeD0iMTUiIGN5PSI5IiByPSIyLjEiIGZpbGw9IiNGMjJGNDYiLz48Y2lyY2xlIGN4PSI5IiBjeT0iMTUiIHI9IjIuMSIgZmlsbD0iI0YyMkY0NiIvPjxjaXJjbGUgY3g9IjE1IiBjeT0iMTUiIHI9IjIuMSIgZmlsbD0iI0YyMkY0NiIvPjwvc3ZnPg==" alt="Twilio">
<img src="https://img.shields.io/badge/Supabase-2A1A0E?style=for-the-badge&logo=supabase&logoColor=3FCF8E" alt="Supabase">
<img src="https://img.shields.io/badge/GitHub%20Actions-2A1A0E?style=for-the-badge&logo=githubactions&logoColor=5AA9FF" alt="GitHub Actions">

<br>

</div>

Affirmations on the days you need them. Reminders on the days you forget. Prep cues, water nudges, supplement timing, study check-ins. A working personal-infrastructure project built around one principle: the right text at the right moment is more effective than any app you have to open.

<p align="center"><img src=".github/brand/divider.svg" width="100%" alt=""></p>

## What it will do

- Send scheduled SMS messages to a single recipient (the owner)
- Pull from configurable content libraries (affirmations, prep cues, reminders)
- Schedule per-library cadence (e.g., affirmations daily at 7am, water nudges every 2 hours during work, study check-ins weekday evenings)
- Allow inbound replies to log mood / completion / streak
- Vary message wording so the texts don't become wallpaper

<p align="center"><img src=".github/brand/divider.svg" width="100%" alt=""></p>

## What it will NOT do

- Send marketing
- Connect to other humans
- Store anything beyond what's necessary to function

This is a one-user tool, by design.

<p align="center"><img src=".github/brand/divider.svg" width="100%" alt=""></p>

## Planned stack

Python · Twilio Programmable Messaging · Supabase (cron + storage) · GitHub Actions (scheduler) · .env for secrets

<p align="center"><img src=".github/brand/divider.svg" width="100%" alt=""></p>

## Architecture sketch

```
[ content library (yaml) ]
            │
            ▼
[ GitHub Actions cron ] ──► [ python sender ] ──► [ Twilio API ] ──► [ SMS ]
            │                                            │
            ▼                                            ▼
       [ Supabase ] ◄─────────────────── [ inbound reply webhook ]
```

<p align="center"><img src=".github/brand/divider.svg" width="100%" alt=""></p>

## Why it lives here

Personal infrastructure deserves to be built in public. The README ships first. The working version ships when it's ready.

<p align="center"><img src=".github/brand/divider.svg" width="100%" alt=""></p>

## Status

**Pending.** README is the spec; implementation in progress.

<p align="center"><img src=".github/brand/divider.svg" width="100%" alt=""></p>

<p align="center">
  <a href="https://juniajanvier.com"><img src=".github/brand/footer.svg" width="520" alt="Junia Janvier · The Education Alchemist · Providence, RI"></a>
</p>
