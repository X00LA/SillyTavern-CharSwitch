# Char Switch for SillyTavern

A lightweight SillyTavern extension that adds a quick character-switch popup for fast navigation between recent characters and chat groups.

## Overview

This project enhances the SillyTavern interface by providing an easy way to switch active characters without leaving the main chat view. It displays a context menu from the right-side navigation trigger, showing recent characters and groups with avatars and optional favorite highlighting.

## Features

- Quick character switching from the SillyTavern navigation area
- Supports both individual characters and group chats
- Displays avatars for characters and group avatars when available
- Optional favorite support to prioritize or filter important characters
- Configurable number of entries shown in the menu
- Works with the standard SillyTavern layout and Discord-like layouts

## Installation

1. Clone or download this repository.
2. Copy the project folder into your SillyTavern extensions directory.
3. Restart SillyTavern.
4. The extension will be loaded automatically via `manifest.json`.

## Usage

- Open the SillyTavern UI.
- Right-click the character switch trigger in the navigation area.
- Choose a character or group from the popup menu.
- The selected character or group becomes active immediately.

## Configuration

The extension exposes a small set of options through the SillyTavern extension settings object:

- `showAvatar`: Show avatars in the switch menu
- `showFavorites`: Sort favorite characters to the top
- `onlyFavorites`: Restrict the menu to favorite entries
- `highlightFavorites`: Visually highlight favorite characters
- `numCards`: Maximum number of cards displayed in the menu

## Project Structure

- `manifest.json` — extension metadata required by SillyTavern
- `index.js` — core logic for the switch menu and character selection
- `style.css` — default styling for the popup UI
- `style.less` — Less source for styling

## Notes

This repository is built specifically for SillyTavern and depends on the app’s runtime APIs and extension system.
