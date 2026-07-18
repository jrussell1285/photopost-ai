# PhotoPost AI — Daily v2

A phone-friendly app that turns everyday photos into natural, accurate social-media posts.

## What changed in v2

- Quick Post mode for daily use
- Fine Tune mode for tone, length, emoji, hashtag and accuracy control
- Better priority for user context and exact facts
- Careful reading of visible labels, prices, dates and measurements
- Explicit warnings when a detail should be checked
- One-tap rewrites: shorter, casual, less salesy, funny, professional and fresh
- Per-profile writing voice and examples
- Learns locally from captions the user approves
- Avoids repeating recent captions
- Suggested accessibility description
- Stronger platform-specific hashtag limits
- Stronger rules against invented purchases, tastings, locations and product claims

## Update an existing GitHub/Netlify install

Replace the existing `photopost-app.zip` file in the GitHub repository with the new v2 `photopost-app.zip`.

Netlify will automatically deploy the updated ZIP using the existing `netlify.toml`.

Because this version changes the service-worker cache name, the phone should receive the new interface after the deployment is published. If an installed copy still shows the old screen, close it completely and reopen it, or refresh the Netlify address in Chrome once.

## Privacy

- The OpenAI key remains in Netlify environment variables.
- Photos are resized before upload.
- This starter app does not permanently store uploaded photos.
- Profiles, approved style examples, recent caption text and drafts are stored only in the browser on that device.
