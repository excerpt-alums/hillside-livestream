# hillside-livestream

Serves the current Hillside Covenant Church YouTube livestream/recording metadata for the website watch page.

## Consumers

- **SquareSpace watch page** — Code Injection block fetches `current-livestream.json` and embeds the video.

## Weekly update flow

1. `publish-to-youtube.js` creates the 9 AM livestream broadcast and returns a video ID
2. Update `current-livestream.json` with the new `video_id`, `youtube_url`, and `service_date`
3. Commit and push — GitHub Pages serves the new JSON within ~1 minute
4. After post-production: swap `video_id` to the polished video and push again

## Endpoint

```
https://excerpt-alums.github.io/hillside-livestream/current-livestream.json
```
