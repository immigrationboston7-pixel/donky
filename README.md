# Donkey Kong Multi Screen (iPhone)

A fan-made tribute to the 1982 Nintendo Game & Watch **Donkey Kong** (DK-52), the
first clamshell "Multi Screen" LCD handheld, rebuilt as an iPhone web app.
It's plain HTML, CSS and JavaScript with no build step and no dependencies. It
runs full screen and offline once you add it to your Home Screen.

## Play it on your iPhone

1. Host the folder over HTTPS. The quickest way is GitHub Pages: in the repo, open
   **Settings → Pages**, set **Source** to **GitHub Actions**, then merge to `main`.
   The included workflow (`.github/workflows/pages.yml`) publishes the site.
2. Open the site in **Safari** on your iPhone.
3. Tap **Share → Add to Home Screen**. Launch it from the new icon to play full
   screen with no browser bars. It keeps working offline.

To try it on a computer, open `index.html` in a browser, or run
`python3 -m http.server` and visit `http://localhost:8000`.

## How to play

Mario starts at the bottom left of the lower screen. Climb the girders up to
the top screen, dodging the barrels Donkey Kong throws, then use the crane to
cut the four wires holding up DK's platform. Cut all four and DK falls.

| Control | Touch | Keyboard |
|---|---|---|
| Move / climb | D-pad | Arrow keys |
| Jump | JUMP | Space, Z or X |
| Start Game A (normal) / Game B (fast) | GAME A / GAME B | 1 / 2 |
| Clock (attract mode) | TIME | T |
| Sound on/off | SOUND | M |

* **Barrels:** jump over them. A barrel is worth 1 point on the lower screen and 2 on the top screen.
* **Sliding girder:** a girder slides back and forth over the middle floor. Jump under it and Mario bonks his head (a miss).
* **Crane:** at the top floor, stand at the switch (the 3rd spot) and press **Up**. The hook swings over and back twice, then stops.
  Step to the edge and press **JUMP** when the hook swings all the way to the left. If you grab it you cut a wire, and if you miss you fall.
* **Wire points:** a wire is worth 20, 15, 10 or 5 points depending on how fast you got there. If you dawdle, the barrels speed up.
* **DK falls:** cutting all four wires drops DK for a 20 point bonus. The next round is faster.
* **300 points:** if you have no misses you get *Chance Time*, where the score flashes and all points count double until your next miss. If you do have misses, they are cleared.
* **Misses:** three misses end the game. The score display has three digits, so it rolls over after 999. Your high score is saved on the device.

## Files

* `index.html` holds the whole game. Every LCD element is a fixed segment, and unlit segments are drawn as faint "ghosts" like a real LCD.
* `manifest.webmanifest`, `sw.js` and `icons/` provide the Home Screen install and offline cache.

## Sources for the original rules

* [Donkey Kong (Game & Watch), Super Mario Wiki](https://www.mariowiki.com/Donkey_Kong_(Game_%26_Watch))
* [Donkey Kong, Game & Watch Wiki](https://gameandwatch.fandom.com/wiki/Donkey_Kong)
* [Donkey Kong, NinDB](https://nindb.net/gw/donkey-kong/index.html)
* [DK-52 maximum points discussion, gameandwatch.ch forum](https://gameandwatch.ch/en/game-and-watch-forum/47-game-watch-board/5730-donkey-kong-dk-52-and-maximum-points-issue.html)

The screen layout and timings here are a reinterpretation, not a pixel copy of the original.

*Fan-made tribute. Not affiliated with or endorsed by Nintendo. Donkey Kong and Game & Watch are trademarks of Nintendo.*
