# socialmanager-oauth

Static OAuth redirect page for a self-hosted SocialManager instance.

TikTok does not accept `localhost` as an OAuth redirect URI. TikTok redirects to
`https://schwifty00.github.io/socialmanager-oauth/tiktok/`, and the page forwards
`code` and `state` to `http://100.112.29.35:5175/api/v1/accounts/oauth/tiktok/callback` (SocialManager frontend via Tailscale; Vite proxies /api to the API).

The authorization code is single-use and can only be exchanged with the app's
client secret, which stays on the SocialManager server.
