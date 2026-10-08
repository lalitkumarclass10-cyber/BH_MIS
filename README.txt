LALIT_BH — FINAL BUILD
======================

This is the final consolidated PWA package for the Eye Hospital Business Command Center.

Included:
- Full daily data entry using the complete LALIT_BH base fields
- Automatic Total OP and ARP calculations
- Monthly targets for all targetable metrics
- Monthly Last Year baseline for all targetable metrics
- Actual vs Target vs LY analytics
- Business Lever dashboard
- Revenue mix, target achievement and trend charts
- Conversion metrics
- Staff leave tracker
- JSON backup/restore and CSV export
- Offline PWA support
- Secure AI integration architecture (server-side endpoint)

IMPORTANT AI SECURITY:
Do NOT put an OpenAI API key into index.html or browser JavaScript. The browser calls a secure server endpoint. An example Cloudflare Worker is included in ai-worker/.

AI WORKER SETUP (one-time):
1. Create a Cloudflare Worker.
2. Deploy ai-worker/worker.js.
3. Add Worker secret OPENAI_API_KEY.
4. Optionally add OPENAI_MODEL (default gpt-5.6-luna).
5. Copy the Worker URL into LALIT_BH → Settings & AI → Secure AI endpoint URL.
6. Tap Analyse my data from the Dashboard.

The worker uses the OpenAI Responses API server-side and returns a structured management analysis.

HOSTING:
The front-end works on GitHub Pages, Netlify, Cloudflare Pages, etc. The AI worker is separate because GitHub Pages cannot safely hold a private API key.
