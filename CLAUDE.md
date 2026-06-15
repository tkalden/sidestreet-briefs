# SideStreet Briefs — Claude Instructions

## Git
- Always commit directly to **master** (not feature branches).
- Before pushing, configure git credentials using the `GITHUB_TOKEN` environment variable:
  ```
  git remote set-url origin "https://$GITHUB_TOKEN@github.com/tkalden/sidestreet-briefs.git"
  git push origin master
  git remote set-url origin "https://github.com/tkalden/sidestreet-briefs.git"
  ```

## Brief output
- Save markdown brief to `~/Documents/MarketBrief/brief-YYYY-MM-DD.md`
- Update `index.html` in the repo root with today's HTML brief, then commit + push to master.

## Delivery
- No push notifications needed — GitHub commit is the deliverable.
- Twilio WhatsApp/SMS: send digest if `TWILIO_ACCOUNT_SID`, `TWILIO_AUTH_TOKEN`, `WHATSAPP_FROM`, `WHATSAPP_GROUP_TO`, and `TESS_PHONE` env vars are present.
