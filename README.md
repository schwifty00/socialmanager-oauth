# socialmanager-oauth

Static OAuth redirect page for a self-hosted SocialManager instance.

TikTok does not accept `localhost` as an OAuth redirect URI. TikTok redirects to
`https://schwifty00.github.io/socialmanager-oauth/tiktok/`, and the page forwards
`code` and `state` to `https://localhost:8000/api/v1/accounts/oauth/tiktok/callback`.

The authorization code is single-use and can only be exchanged with the app's
client secret, which stays on the SocialManager server.
