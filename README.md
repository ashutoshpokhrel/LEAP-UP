# 🐸 LEAP-UP

A vertical platformer game built with **C++** and **SFML 3.x**, where you jump your way up through increasingly challenging platforms, dodge fireballs, and collect powerups to survive as long as possible.

---

## 🎮 Gameplay

- Jump between platforms to climb as high as you can
- Avoid **fireballs** that fly across the screen
- Land on **thorn platforms** and you're dead instantly
- **Disappearing platforms** vanish after you jump off them
- **Moving platforms** keep things unpredictable
- Collect **Shield** and **Jetpack** powerups to gain an edge
- Your high score is saved between sessions

---

## 🗂️ Project Structure

```
LEAP-UP/
├── README.md
├── .gitignore
├── highscore.txt          # Saved locally at runtime (starts at 0)
│
├── src/
│   ├── game.cpp / game.hpp
│   ├── manual.cpp / manual.hpp
│   ├── credits.cpp / credits.hpp
│   ├── shield.hpp
│   ├── jetpack.hpp
│   ├── fireball.hpp
│   ├── floating.hpp
│   └── pixelcollision.hpp
│
└── assets/
    ├── player.png / player2.png
    ├── jetpackplayer.png
    ├── plat1.png / plat2.png / plat3.png
    ├── bg1.png
    ├── fireball.png
    ├── shield.png
    ├── jetpackicon.png
    ├── pause.png / resume.png / resume2.png
    ├── quit.png / exit2.png
    ├── over.png / again.png / again2.png
    ├── manualp.png
    ├── creditsp.png
    ├── back.png
    └── pixel.ttf
```

---

## 🛠️ Building

### Requirements

- [SFML 3.x](https://www.sfml-dev.org/download/) (Graphics, Window, System, Audio, Network)
- A C++17-compatible compiler (g++, MSVC, clang++)

### Compile (g++ example)

```bash
g++ src/game.cpp src/manual.cpp src/credits.cpp -o LeapUp \
    -lsfml-graphics -lsfml-window -lsfml-system -lsfml-audio \
    -std=c++17
```

### Run

> **Important:** Always run the executable from the **project root** (the folder containing `assets/` and `highscore.txt`), otherwise the game won't find its assets.

```bash
./LeapUp
```

On Windows, make sure the SFML `.dll` files are either in your PATH or in the same folder as the executable.

---

## 📁 Notes

- `highscore.txt` is auto-created/updated at runtime. The repo includes a default version with `0`.
- `.dll` files are **not** included — install SFML separately for your platform.
- Pixel-perfect collision is handled via `pixelcollision.hpp` using alpha-channel checks.

---

## ⬇️ Download & Play

No setup required! Just download the latest release:

👉 [Download LEAP-UP v1.0](https://github.com/ashutoshpokhrel/LEAP-UP/releases/tag/v1.0)

1. Extract the zip
2. Double-click `LEAP-UP.exe`
3. Play!

> Windows only. No installation needed.

---

## 👾 Credits

See the in-game Credits screen, or check `credits.cpp`.
