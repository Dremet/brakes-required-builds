# Brakes Required — builds for Windows and macOS

**Brakes Required** is a semi-realistic 3D low-poly racing game for PC.
Website: [dremet.games](https://dremet.games)

This repository holds the downloadable game builds only. It holds no game
source code and no reusable art source files.

## Download

Get the newest build from the
[Releases page](https://github.com/Dremet/brakes-required-builds/releases).

| Platform | File | Requirements |
| --- | --- | --- |
| Windows | `BrakesRequired-<version>-win64.zip` | Windows 10 or 11, 64-bit |
| macOS | `BrakesRequired-<version>-macos.dmg` | macOS 11 or newer (Apple silicon), macOS 10.15 or newer (Intel) |
| Linux | — | coming soon |

## Install and start

### Windows

1. Unzip the file into an empty folder.
2. Start `BrakesRequired.exe`.

There is no installer. To remove the game, delete the folder.

Windows can show a SmartScreen warning, because the build has no code
signature. Select **More info**, then **Run anyway**.

### macOS

1. Open the `.dmg` file.
2. Drag **Brakes Required** onto the **Applications** folder.
3. Start the game from Applications.

The build is not notarized by Apple, so macOS blocks the first start with a
message that it cannot check the app. To allow it once:

1. Try to start the game and close the message.
2. Open **System Settings → Privacy & Security**.
3. Scroll down to the note about **Brakes Required** and select **Open Anyway**.
4. Confirm with your password or Touch ID.

To remove the game, move it from Applications to the Trash.

## Saved data

Best times, settings and your online nickname stay when you install a newer
build. They live outside the game folder:

- Windows: `%APPDATA%\Godot\app_userdata\Brakes Required`
- macOS: `~/Library/Application Support/Godot/app_userdata/Brakes Required`

## Report a problem

The version is in the bottom left corner of the screen. The field is
selectable: click it and press Ctrl+C (Cmd+C on macOS) to copy the exact string.

Open an [issue](https://github.com/Dremet/brakes-required-builds/issues) and
give that version string with your report.

## Source code

The game source code is private. It is not published here.
