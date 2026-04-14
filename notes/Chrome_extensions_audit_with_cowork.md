# 2026-04-12
<!-- Tool: Claude · Model: claude-sonnet-4-6 · Interface: Cowork Mode (Claude Desktop App) -->
> **Essence:** Claude can't audit your browser directly, but give it your extension list and it will research every one — and it found two actively harmful ones I removed today from my chrome browser.

## What I learned
1. Claude cowork (as of April 12, 2026) cannot connect to a live Chrome browser — it has no access to installed extensions, open tabs, cookies, or real-time browser state. It does have Google Drive and Google Calendar connectors, neither of which solves my current problem.
2. You can still get a full extension privacy audit by pasting your extension list into Cowork — Claude will research each one via web search and give risk ratings (Low / Medium / High) plus data collection details.
3. PayPal Honey had a major scandal in late 2024 (affiliate theft, coupon manipulation, 6M+ users lost, class action filed), and Perplexity AI Companion had a class action filed in March 2026 for sending conversations to Meta and Google — both were identified and removed today.

## What I applied
- Pasted 18 Chrome extensions and received a risk-tiered audit with actionable recommendations.
- Removed PayPal Honey, Perplexity AI Companion, and Evernote Web Clipper based on findings.

## What was confusing
- It's not obvious Claude can't connect to Chrome — the capability feels like it should exist given its other agentic features.

## Next thing to try
- Export cookies via Cookie-Editor and upload to Claude to see if it can audit them.
- Check if Claude in Chrome (the browsing agent) can inspect extensions or cookies in real time.
