# OpenTube TV player page

A single static page, `player.html`, used by **OpenTube TV**, the Samsung Tizen edition of
[OpenTube](https://github.com/3n9d/opentube).

YouTube's embedded player requires the embedding app to identify itself with an HTTP
Referer. A Tizen TV app runs from local files and cannot send one, so YouTube refuses
playback with error 153. OpenTube TV therefore frames this page, served over HTTPS from
GitHub Pages, and the page contains YouTube's embedded player.

- YouTube's **official, unmodified** embedded player (`youtube-nocookie.com/embed`).
- Nothing is drawn over the player. Ads and YouTube's controls stay as YouTube serves them.
- The TV app sends only documented IFrame API commands (`playVideo`, `pauseVideo`, `seekTo`, volume).
- Only an 11-character video id is accepted (`player.html?v=<id>&t=<seconds>`).
- The page downloads, stores and proxies nothing. It has no analytics and no server-side code.

OpenTube is not affiliated with YouTube or Google.

Licence: GPL-3.0-or-later (see [LICENSE](LICENSE)).
