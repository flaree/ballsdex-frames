# Changelog

All notable changes to the Frames package are documented here.

---

## 0.0.1 — 2026-05-12

Initial release.

### Added

- `FrameBall` proxy model providing a dedicated **Frames** section in the BallsDex Django admin.
- Custom add and change views for managing date-keyed frame entries stored in `Ball.capacity_logic`.
- Date-range support — a single form submission can write frames across multiple consecutive days (`MM-DD-YYYY` keys).
- Spawn art override — replaces the wild-card image when a ball spawns in a channel.
- Card art override — replaces the collection card artwork rendered by `draw_card`.
- Catch phrase and credits fields — appended to the catch message and displayed on the card for the duration of the frame.
- `🖼️` badge in the `/balls` collection menu for balls carrying a frame card.
- `frame` filter injected into `FilteringChoices` so players can filter their collection to balls with an active frame.
- Runtime monkey-patching of `BallInstance.save`, `BallInstance.objects.acreate`, `BallSpawnView.spawn`, `image_gen.draw_card`, `CountryballFormatter.format_page`, and `filter_balls` — all patches are cleanly restored on cog unload.
