# Waitlist for GitHub

Idea: It's currently not super straightforward to release ideas early and make people come back. GitHub has a `watch` functionality but there's no easy way to message all people.

Requirements:

- `GET /owner/repo Accept: image/*`: Returns `og:image` for the subscribers page.
- `GET /owner/repo Accept: text/*`: Anyone can see who subscribed here, authenticated owner can see emails as well. It offers prompts to email everybody, tag everybody on GitHub, or tag everybody on X with URLs to actually do it.
- `GET /owner/repo/subscribe?type=x|github`: Page with either x-oauth or github-oauth that subscribes either xhandle or email to the repo subscribe list.
- `GET /owner/repo/unsubscribe`: Logged in user will be removed from the subscribe-list.
- `GET /owner/repo/badge`: returns a SVG badge that can be added to the repo to subscribe. Shows amount of subscribers.

The cool thing about this, is that you can just add it to your readme to collect people that want to stay updated about this.
