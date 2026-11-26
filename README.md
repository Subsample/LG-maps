# LG Maps

Interactive maps of student network groups, built as single self-contained HTML files.

| Map | Live | File |
| --- | --- | --- |
| ESTIEM Local Groups (Europe) | https://subsample.github.io/LG-maps/estiem/ | `estiem/index.html` |
| IAESTE member countries (world) and local committees (Germany) | https://subsample.github.io/LG-maps/iaeste/ | `iaeste/index.html` |

Each map is one HTML file with its data and geometry built in. There is no build step and no backend.

## Embedding

Drop an iframe into the page, e.g. in an Elementor **HTML** widget:

```html
<iframe src="https://subsample.github.io/LG-maps/estiem/" style="width:100%;height:80vh;min-height:560px;border:0;border-radius:12px" loading="lazy" title="ESTIEM Local Groups Map"></iframe>
```

- `iaeste/#germany` opens the IAESTE map in the Germany view, `#world` in the world view.
- When embedded, the plain mouse wheel and one-finger swipes scroll the host page. Zooming takes Ctrl/⌘ + scroll or two fingers. Add `?coop=0` to the URL to turn this off.

## Hosting it yourself

You are welcome to host a copy on your own server, for example on estiem.org. Copy the folder (or just its `index.html`) to any static web host and point the iframe at it. Keep the `LICENSE` file or the copyright notice with it.

The files load three things from external servers:

- d3 7.9.0 from cdnjs.cloudflare.com
- topojson-client 3.1.0 from cdn.jsdelivr.net
- fonts from Google Fonts

On a site that must not contact third-party servers (e.g. for GDPR reasons), download these files and change the `<script>` and `<link>` URLs at the top of the HTML to local copies.

## License

The code is under the [MIT License](LICENSE): copy, modify and host it freely, as long as the license notice stays with it.

Not covered by this license:

- **Names and logos.** The ESTIEM and IAESTE names and logos (including the IAESTE emblem shown in the IAESTE map) belong to their organisations.
- **Third-party components.** These keep their own licenses:
  - d3 and topojson-client: ISC license.
  - World geometry: [Natural Earth](https://www.naturalearthdata.com/) (public domain), via the world-atlas package (ISC).
  - German state outlines: from public-domain sources ([deutschlandGeoJSON](https://github.com/isellsoap/deutschlandGeoJSON), Unlicense).
  - Fonts from Google Fonts: SIL Open Font License.

Group lists, links and contact details were taken from public pages (estiem.org, my.estiem.org, iaeste.org, iaeste.de) in November 2026. They change over time, so check them before relying on them.
