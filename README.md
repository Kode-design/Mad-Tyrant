# Mad-Tyrant
A game called Mad Tyrant
# Mad Tyrant

A dark-fantasy 2D action platformer. Rise as **Mangus Ribspreader** — buried for ten thousand years, woken by something older than the wards that bound him — and carve a path back to the world that forgot his name.

The whole game is a single `index.html` file: pixel-art sprites generated in code, procedural WebAudio sound, and a hand-built physics + combat loop. No build step. No dependencies. Just open it.

## Play

Open `index.html` in any modern browser, or serve it locally:

```
python3 -m http.server
# then visit http://localhost:8000
```

## Controls

| Key | Action |
| --- | --- |
| `A` / `←` · `D` / `→` | Move |
| `S` / `↓` | Fast-fall while airborne |
| `SPACE` / `W` | Jump · hold for a higher leap (apex hangtime) |
| `A`/`D` + `SPACE` against a wall | Wall-jump · cling, kick, refund your air dash |
| `J` / `X` | Attack · hold to charge a heavy strike |
| `SHIFT` | Dash · 1 free air-dash · refunded when you hit an enemy |
| `ESC` | Pause |

## Movement design

Movement is the heart of the game and built for chaining:

- **Coyote time** + **jump buffer** so jumps that *feel* on time *are* on time.
- **Apex hangtime** — gravity softens at the peak of your jump while the button is held, giving you a beat to read enemies.
- **Air dash** — one in-air dash that **refreshes on landing** *or* on a successful hit, rewarding aggressive aerial play.
- **Wall slide & wall jump** — push into a wall in mid-air to grip it; jump off to launch sideways and reset your air dash.
- **Fast fall** — hold down to drop hard and skip the apex when you need to commit.
- **Landing squash, run dust, dash afterimages, friction sparks** — every action prints to screen so the world reacts to you.

## License

MIT — see `LICENSE`.
