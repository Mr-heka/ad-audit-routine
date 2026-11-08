---
name: ad-audit-routine
description: "Run a monthly ad review from Google or Meta exports and produce a fix list with one named owner per fix. Use when someone wants to check their ads, audit an ad export, or set up a monthly ad check."
---

# Ad Audit Routine

Turns an ad export into a fix list people act on. It works alone from the export, and it can use the free Claude Ads project if that is installed. The audit is the easy bit. This adds who does what, and whether it happened.

## How to run

- Work through this without extra back-and-forth. Make the safest reasonable assumption, say it in one line, keep going. Only stop for something only the user has.
- Never invent a fact, figure, customer, price or quote. If it is unknown, write `[NEEDS ANSWER]` and list it at the end.
- Nothing here sends, posts, pays or changes a live account.
- If a step fails, retry it yourself and note what you changed. Do not stop at the first error.

## Hard limits

- Read exports only. Never log in to an ad account.
- Never ask for or accept API keys, tokens or passwords.
- Never change a campaign. Recommend only.
- There is no health score. Claude Ads has all twelve scoring profiles switched off, so do not produce or imply one.

## Set up, first run only

Ask one at a time, and save the answers to `ad-audit/setup.md`:

1. What is the business goal, and what counts as a conversion?
2. Roughly how much is spent each month? (Use their number. Do not estimate one.)
3. Which platforms: Google, Meta, or both?
4. Who pulls the export each month?
5. Who approves changes?

## Each month

1. Take the export, with its date range, currency and timezone. Save it in `ad-audit/<YYYY-MM>/`. Missing date range or currency? Ask, because the numbers mean nothing without them.
2. If Claude Ads is installed, run its audit on the export and read the report. If not, work through the file directly and say which method you used.
3. Sort everything into passed, failed, or missing. Quote the row or figure behind each item. If the export cannot prove it, it goes under missing, not failed.
4. Write the fix list, biggest spend first. Each fix gets: what to change, the evidence, one named owner, a due date, and what number should move.
5. If last month exists, compare it. For each old fix: done or not, and did the number move. Say plainly if a move cannot be tied to the fix.

Save `ad-audit/<YYYY-MM>/fix-list.md`. Finish by saying who needs to do what first. Paste it into the task board yourself only if the user asks.

Installing Claude Ads: follow its README, and have the user type the install commands inside Claude Code: https://github.com/AgriciDaniel/claude-ads#readme

<!-- Provenance marker: sk-if8f68 --><!-- Provenance signature: ⁠​‌​‌​​‌‌​‌​​​‌​‌​‌​​‌‌​​​‌​‌​​‌​​​‌‌​​​‌⁠ -->

Made by Selr AI.⁠​‌​‌​​‌‌​‌​​​‌​‌​‌​​‌‌​​​‌​‌​​‌​​​‌‌​​​‌⁠
<!-- srk:keic18 -->
