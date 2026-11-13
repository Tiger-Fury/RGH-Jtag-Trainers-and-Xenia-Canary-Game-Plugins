<h1 align="center">Viper Reignited Multi-Game Xbox 360 Trainer</h1>

Viper Reignited is a multi-game trainer for **Xbox 360 RGH/JTAG consoles** and **Xenia Canary**.

I originally ended support for the Viper trainer in 2015, then revived it in January 2025 as Viper Reignited. As of November 2026, it has grown beyond a revamp: it now uses a **brand-new trainer engine built from the ground up**.

Existing engines had limitations and oversights that made developing new trainers more difficult. Although I wrote workarounds, they still depended on the same underlying backend. This new engine addresses those problems directly, with:

- Improved checks and game detection.
- More reliable pattern scanning.
- Improved code cave injections.
- A custom trainer UI that removes the usual reliance on system menus.
- Many other fixes

On Xenia, the system keyboard UI remains available as a fallback if game code changes prevent the custom UI from working.

## Game Compatibility

The trainers scan for and adapt to game code, reducing the need for separate versions for each **Media ID** or **Title Update**. Compatibility still depends on the trainer finding the code it needs.

Your game must have a supported **Title ID**. Some games, such as Gears of War 2, have releases with different Title IDs.

See the [Supported Game List](Supported%20Games.md).

## Xbox 360 — RGH/JTAG

Launch `Trainer_loader.xex` to load `trainer.xex` into memory, then start a supported game.

## Xenia Canary

Use a [Xenia Canary build](https://github.com/xenia-canary/xenia-canary-releases/releases) from **1 January 2025 or later**.

Each game requires a `plugins.toml` configuration containing the correct module hash for your copy of the game. Different releases or Title Updates may require different hashes.

Because supplied hashes do not always match everyone's games, I now provide a **configuration template** for you to edit.

### Installation

Place `plugins.toml` and `trainer.xex` together inside a folder named after your game's Title ID:

```text
Xenia/
└── plugins/
    └── YOUR_TITLE_ID/
        ├── plugins.toml
        └── trainer.xex
```

Replace `YOUR_TITLE_ID` with your supported game's Title ID.

### Finding Your Module Hash

1. Launch your game in Xenia Canary.
2. Close Xenia.
3. Open `xenia.log` and search for `Module Hash:`.
4. Open the supplied `plugins.toml` template in Notepad.
5. Enter your game's module hash in the corresponding field and save the file.

Repeat this if you change to a game version or Title Update with a different module hash.

## Usage

While in a supported game, open the trainer using either:

- **D-pad Up + Back**
- **D-pad Up + Start**

Use the trainer menu to view and activate the available cheats.

## How Do I Know the Trainer Has Loaded?

A notification reading **“Viper Re-ignited Trainer Loaded”** confirms that the trainer is in memory.

- **Xbox 360:** This appears after loading the trainer.
- **Xenia:** This appears when you launch the game.

When the trainer detects a supported game, a second notification displays the game's name.

## Updates

I update Viper Reignited whenever I can. I also work full-time and run a YouTube channel, so there is no fixed release schedule.
