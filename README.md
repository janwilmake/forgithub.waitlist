# Waitlist for GitHub

Idea: It's currently not super straightforward to release ideas early and make people come back. Regular SaaS does this using a waitlist. GitHub has a `watch` functionality but there's no easy way to message all people with a big update, they would only see actual releases etc.

Requirements:

- `GET /owner/repo Accept: application/json`: Gets
  - details of subscribed (handle(s) and email) sorted on prominence.
  - shows who starred and watched the repo and their GitHub handle + X handle if they have it.
  - Based on that generates several contexts for tagging/emailing people.
  - Extracts X thread URLs to quote after subscribing ("Join the conversation")
- `GET /owner/repo Accept: text/*`: Anyone can see who subscribed here, authenticated owner can see emails as well. It offers prompts to email everybody, tag everybody on GitHub, or tag everybody on X with URLs to actually do it.
- `GET /owner/repo Accept: image/*`: Returns `og:image` for the subscribers page with images of the most prominent people
- `GET /owner/repo/subscribe?type=x|github`: Page with either x-oauth or github-oauth that subscribes either xhandle or email to the repo subscribe list. On success, it'd offer ways to share the product.
- `GET /owner/repo/unsubscribe`: Logged in user will be removed from the subscribe-list.
- `GET /owner/repo/badge?size=default|large`: returns a badge that can be added to the repo to subscribe. Shows amount of subscribers. Can also add images of the people who acutally did subscribe.
- `GET /owner`: returns an overview of all waitlists of the owner with at least one signup.

The cool thing about this, is that you can just add it to your readme to collect people that want to stay updated about this.

Wdyt? comment here: https://x.com/janwilmake/status/1915665981994668188 (waitlist isn't available yet)
