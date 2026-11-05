# NEXA AI — Advanced Dashboard

A browser-based AI assistant dashboard powered by Google's Gemini API and deployable on Vercel without VS Code.

## Project files
- `index.html` — responsive dashboard and chat interface.
- `api/chat.js` — server-side Gemini API endpoint. The API key is never placed in browser code.
- `vercel.json` — Vercel configuration.

## Deploy using only your browser

1. Download and extract `nexa-ai.zip` on your computer.
2. Open your GitHub repository: https://github.com/danielginx2234/nexa-ai
3. Choose **Add file → Upload files**.
4. Upload `index.html` and `vercel.json` from the extracted folder.
5. Create the API file in GitHub: **Add file → Create new file**, enter `api/chat.js`, then copy the contents from the extracted `api/chat.js`. Commit the changes. (If GitHub's upload page accepts folders, you can upload the `api` folder instead.)
6. Visit https://vercel.com/new, sign in with GitHub, import `danielginx2234/nexa-ai`, and deploy.
7. In Vercel, open the project → **Settings → Environment Variables**.
8. Add a variable named `GEMINI_API_KEY` and set its value to your private Gemini API key from https://aistudio.google.com/app/apikey. Do not prefix the name with `NEXT_PUBLIC_`.
9. Save, then redeploy the latest deployment so the environment variable is applied.
10. Open your Vercel URL and test NEXA.

## Important notes
- This starter uses Gemini `gemini-2.5-flash` through a server-side function. The API key is not exposed in the browser.
- Gemini free-tier availability and quotas vary by model, region, account and time. Check Google AI Studio for current limits.
- Vercel Hobby is intended for personal, non-commercial use and has platform limits.
- This starter keeps conversation context in the current browser page only. It does not yet include accounts or persistent chat history.
- Before sharing publicly, add authentication and rate limiting to prevent others from consuming your API quota.
