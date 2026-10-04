# Char Switch for SillyTavern

A lightweight SillyTavern extension that adds a quick character-switch popup for fast navigation between recent characters and chat groups.

## Overview

This project enhances the SillyTavern interface by providing an easy way to switch active characters without leaving the main chat view. Right-clicking the character management button (far right of the top bar) opens a menu of your most recently chatted characters and groups, with avatars and optional favorite highlighting.

## Features

- Quick character switching via right-click on the character management button
- Supports both individual characters and group chats
- Displays avatars for characters, and combined avatars for groups without their own avatar
- Shows the current character's avatar on the character management button
- Optional favorite support to prioritize or filter important characters
- Configurable number of entries shown in the menu
- Works with the standard SillyTavern layout and Discord-like layouts

## Requirements

None. Char Switch only uses SillyTavern's built-in APIs.

It does **not** depend on Trigger Cards or the Costumes server plugin (the dependency on Trigger Cards was removed in version 1.0.1).

## Installation

1. Clone or download this repository.
2. Copy the project folder into your SillyTavern extensions directory.
3. Restart SillyTavern.
4. The extension will be loaded automatically via `manifest.json`.

## Usage

- Open the SillyTavern UI.
- Right-click the character management button at the far right of the top bar (it shows the current character's avatar).
- Choose a character or group from the popup menu. The menu is sorted by most recent chat; the current character or group is left out.
- The selected character or group becomes active immediately.
- Click anywhere outside the menu to close it.

## Configuration

There is no settings panel. The options are stored in SillyTavern's `settings.json` under `extension_settings.charSwitch`:

| Option | Default | Description |
| --- | --- | --- |
| `showAvatar` | `true` | Show the current character's (or group's) avatar on the character management button |
| `showFavorites` | `false` | Sort favorite characters to the top of the menu |
| `onlyFavorites` | `false` | Show only favorites in the menu |
| `highlightFavorites` | `true` | Visually highlight favorite characters in the menu |
| `numCards` | `10` | Maximum number of entries shown in the menu |

## Troubleshooting

**"Failed to retrieve costumes: 404 - Not Found"** – this message does not come from Char Switch. It is shown by the [Trigger Cards](https://github.com/LenAnderson/SillyTavern-TriggerCards) extension when you right-click one of its cards and the [Costumes server plugin](https://github.com/LenAnderson/SillyTavern-Costumes) is not installed. Install the plugin into SillyTavern's `plugins` folder and restart the server, or disable Trigger Cards with `/tc-off`.

## Project Structure

- `manifest.json` — extension metadata required by SillyTavern
- `index.js` — core logic for the switch menu and character selection
- `style.css` — default styling for the popup UI
- `style.less` — Less source for styling

## Notes

This repository is built specifically for SillyTavern and depends on the app’s runtime APIs and extension system.
