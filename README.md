# Brakes Required — builds for Windows, macOS and Linux

**Brakes Required** is a semi-realistic 3D low-poly racing game for PC.
Website: [dremet.games](https://dremet.games)

This repository holds the downloadable game builds only. It holds no game
source code and no reusable art source files.

## Download

Get the newest build from the
[latest release](https://github.com/Dremet/brakes-required-builds/releases/latest).
The download files are listed under **Assets** at the bottom of the release
page; the easiest way is the Downloads section on [dremet.games](https://dremet.games).

| Platform | File | Requirements |
| --- | --- | --- |
| Windows | `BrakesRequired-<version>-win64.zip` | Windows 10 or 11, 64-bit |
| macOS | `BrakesRequired-<version>-macos.dmg` | macOS 11 or newer (Apple silicon), macOS 10.15 or newer (Intel) |
| Linux | `BrakesRequired-<version>-linux-x86_64.tar.gz` | 64-bit x86, Vulkan graphics drivers (new, less tested) |
| Linux (Flatpak) | `BrakesRequired-<version>-linux-x86_64.flatpak` | 64-bit x86, Flatpak, Vulkan graphics drivers (new, less tested) |

Versions marked **Pre-release** are playtest builds.

## Install and start on Windows

1. Unzip the file into an empty folder.
2. Start `BrakesRequired.exe`.

There is no installer. To remove the game, delete the folder.

Windows can show a SmartScreen warning, because the build has no code
signature. Select **More info**, then **Run anyway**.

**Smart App Control** (Windows 11) blocks the game without a **Run anyway**
option, because the build is not code-signed yet. The only way around it is to
turn it off: Windows Security → App & browser control → Smart App Control
settings → Off. On some Windows versions it can only be turned on again by
reinstalling Windows, so decide that for yourself.

## Install and start on macOS

1. Open the `.dmg` file. A window opens with **Brakes Required** and an
   **Applications** folder.
2. Drag **Brakes Required** onto the **Applications** folder. Then eject the
   DMG.
3. Start the game from Applications.

The build is not notarized by Apple, so macOS blocks the first start with a
message that it cannot check the app. To allow it once:

1. Try to start the game and close the message.
2. Open **System Settings → Privacy & Security**.
3. Scroll down to the note about **Brakes Required** and select **Open Anyway**.
4. Confirm with your password or Touch ID, then select **Open**.

macOS remembers this. Later starts need no extra step.

If the message says the app is damaged, run this once in Terminal, then start
the app again:

```
xattr -dr com.apple.quarantine "/Applications/Brakes Required.app"
```

To remove the game, move it from Applications to the Trash.

## Install and start on Linux

1. Download `BrakesRequired-<version>-linux-x86_64.tar.gz`.
2. Unpack it into an empty folder (`tar -xzf BrakesRequired-<version>-linux-x86_64.tar.gz`).
3. Start `./BrakesRequired.x86_64` from a file manager or a terminal.

The game needs Vulkan graphics drivers. Linux builds are new and less tested
than Windows and macOS; please report problems.

### Flatpak

The same game as a single Flatpak file (not on Flathub yet). It needs the
Flathub remote for its runtime (`org.freedesktop.Platform`), which many
distributions already have:

```
flatpak remote-add --user --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak install --user BrakesRequired-<version>-linux-x86_64.flatpak
flatpak run games.dremet.BrakesRequired
```

After the install the game is also in your application menu. There are no
automatic updates: install the next version's file the same way. To remove
it: `flatpak uninstall --user games.dremet.BrakesRequired`.

The Flatpak keeps its own saved data, separate from the tar.gz build (see
below), so it asks for a nickname again. To keep your nickname and times,
copy the tar.gz build's folder into the Flatpak's before its first start.

## Online leaderboards

Since 0.3.0 your laps go to the online leaderboards on
[dremet.games](https://dremet.games/en/leaderboards/). At the first start you
pick a nickname. It cannot be changed later and is shown publicly on the
leaderboards. No email or account is needed. What is stored and why:
[privacy](https://dremet.games/en/privacy/). The game also plays fully
offline; laps upload once you are online again.

## Saved data

Best times, settings and your online nickname stay when you install a newer
build. They live outside the game folder:

- Windows: `%APPDATA%\Godot\app_userdata\Brakes Required`
- macOS: `~/Library/Application Support/Godot/app_userdata/Brakes Required`
- Linux (tar.gz): `~/.local/share/godot/app_userdata/Brakes Required`
- Linux (Flatpak): `~/.var/app/games.dremet.BrakesRequired/data/godot/app_userdata/Brakes Required`

Keep this folder: it holds your online identity. Without it the game asks for
a new nickname.

## Report a problem

Please report bugs in the **#bugs** channel on Discord:
https://discord.gg/2sByBExEwy

The version is in the bottom left corner of the screen. The field is
selectable: click it and press Ctrl+C (Cmd+C on macOS) to copy the exact string.
Give that version string with your report. You can also open an
[issue](https://github.com/Dremet/brakes-required-builds/issues).

## Source code

The game source code is private. It is not published here.
