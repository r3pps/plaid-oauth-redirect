# Plaid OAuth Redirect Page

This repository exists only to host a static Plaid OAuth redirect page for FinanceAI.

## Files

- `index.html` - the redirect landing page

## GitHub Pages setup

1. Create a new public GitHub repository, for example: `plaid-oauth-redirect`
2. Copy `index.html` from this folder into the new repo root
3. Push the repo to GitHub
4. In GitHub, open `Settings` -> `Pages`
5. Under `Build and deployment`, choose:
   - `Source`: `Deploy from a branch`
   - `Branch`: `main`
   - `Folder`: `/ (root)`

After GitHub Pages publishes, your redirect URI will usually be:

- `https://<your-github-username>.github.io/<repo-name>/`

Example:

- `https://r3pps.github.io/plaid-oauth-redirect/`

## Plaid setup

1. Add the published URL as an allowed redirect URI in the Plaid Dashboard
2. Set the same URL in FinanceAI:

```env
PLAID_REDIRECT_URI=https://r3pps.github.io/plaid-oauth-redirect/
```

3. Restart the FinanceAI backend after updating `.env`
