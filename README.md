# Bank Heist Defender

**Shoot the robbers. Don't shoot the civilians.**

A fast 2D touch shooting gallery for phones and tablets, played upright in portrait. You're the guard on duty at the First National Bank: robbers and civilians pop up from behind the counters, desks, sofas, doorways and the open vault, and you have a split second to decide who to tap.

### [Play it now at bank-heist-defender.vercel.app](https://bank-heist-defender.vercel.app/)

> Can you beat the dev's high score of **91,050**?

---

## How to play

| | Who | What to do |
|---|---|---|
| 🔴 | **Robber**: dark clothes, red ski mask, red outline, money bag | Shoot! |
| 🟠 | **Bomber**: orange jumpsuit, lit bomb, glowing orange outline | Shoot him twice before the fuse runs out |
| 🟢 | **Civilian**: bright clothes, tie or briefcase, green outline | Hold fire! One shot and it's game over |

They pop up at 9 spots spread down the screen: the office door, the vault and the exit at the back, two teller counters, two desks, and two waiting-room sofas right in front of you.

The game ends when you **shoot a civilian** or when the **clock runs out**.

### Scoring

- **+100** per robber, **+50** bonus for a **headshot** (top of the body)
- **Combo multiplier** from x1 up to **x5**: it goes up one step every 3 hits in a row. A miss resets it.
- Your high score is saved in your browser.

### The clock

- You start with **25 seconds**, and the clock can hold up to **45**.
- Every robber you hit adds **+1s** (headshot **+1.75s**).
- Under 10 seconds the timer turns red, pulses and starts ticking.

### Ammo

- Your gun holds **5 bullets**. Every shot uses one, hit or miss.
- **Headshots are free**: the bullet is refunded (**+AMMO**).
- When the magazine is empty the gun **reloads automatically** (1.2 seconds). You can't shoot while reloading, and the clock keeps running.

### The Bomber

A rare special robber that gets more common as you level up (2% at level 1, up to 15%). Only one shows up at a time.

- He stays up for **5 seconds** with a countdown above his head, and his bomb beeps faster as the fuse burns down.
- It takes **2 hits** to take him down.
- **Defuse it**: **+500 points** (times your combo) and **+3 seconds**.
- **Too slow**: the bomb explodes. You lose **600 points** and **5 seconds**, and your combo resets.

### Berserk Mode

Hit **15 robbers in a row** without missing to go **BERSERK** for 5 seconds:

- Your pistol becomes a **minigun**. **Hold your finger down** (or the mouse button) to fire about 15 rounds a second, and drag to sweep across the bank.
- **Unlimited ammo**, and misses don't count against you.
- Only robbers appear, and lots of them. Each kill is worth **+200** and **+0.5s**.
- When it ends you get a full magazine back, and the streak starts again from zero.

### Levels

You go up a level every **4 robbers**. Each level makes the bank a little more dangerous:

- Characters pop up and duck faster and stay visible for less time.
- More of them appear at once (up to 5), and civilians show up more often.
- From level 2 they start appearing in quick **bursts**, and every few levels a **wave** of 3–4 pops up within half a second.

### End of game stats

Final score, high score, robbers caught, accuracy, highest level, longest kill streak, bombs defused, bombs exploded, and how many times you went berserk.

---

## Controls

| Action | Phone / tablet | Computer |
|---|---|---|
| Shoot | Tap the target | Click |
| Minigun (Berserk) | Hold your finger down and drag | Hold the mouse button |
| Pause | Pause button | `P` or `Esc` |
| Mute | Speaker button | `M` |
| Start / play again | Tap **PLAY** | `Enter` or `Space` |

### Playing on a phone or tablet

- The game is **portrait only**: hold your device upright. If you turn it sideways the game pauses and asks you to turn it back.
- Tall phones get a taller view of the bank; tablets get a centred portrait screen.
- On Android, tapping **PLAY** switches to fullscreen and locks the screen upright.
- On iPhone, use **Share → Add to Home Screen** to play full screen without the browser bars.
- On a computer the game still works: it shows as a portrait screen in the middle of the window and you play with the mouse.

---

## Run it yourself

The whole game is a single file, [`index.html`](index.html), with no images, libraries or build step. Everything is drawn in code and every sound is generated live.

1. Download `index.html`.
2. Open it in any modern browser (Chrome, Edge, Firefox or Safari), ideally on your phone.

That's it. To host it, put `index.html` on any static host (the live version runs on Vercel).

## Built with

- **HTML5 Canvas** for all the graphics: the bank, the characters, the guns, explosions and effects
- **Web Audio API** for every sound: gunshots, the minigun, reloads, bomb beeps and explosions
- **Plain JavaScript**, with no frameworks or dependencies
- `localStorage` for the high score and sound setting
