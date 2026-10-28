# LE Auto Record

Watching a programme and deciding later to keep it should not mean losing it when the live buffer disappears. LE Auto Record turns programmes watched long enough on OpenPLi into normal recordings, so they can be found again in the movie folder on a disk or NAS. It makes everyday viewing easier to retain without scheduling a separate recording for every show.

## Tech stack

| Layer | Technologies |
|---|---|
| Receiver platform | Enigma2; OpenPLi |
| Plugin | Python |
| Recording and storage | MPEG transport stream; local disk; CIFS network shares |

## Keep the programmes you actually watch

Automatic saving uses the receiver's live TV buffer to preserve watched programmes as ordinary `.ts` recordings. A minimum viewing duration helps distinguish a programme worth keeping from a brief stop while changing channels. Saving can be enabled or disabled from the plugin's setup screen.

The recording routine follows the programmes the viewer spends time watching. It is intended to make useful viewing material easier to retain without requiring every session to begin with a separate manual recording decision.

## Organise recordings around the programme guide

Programme-change splitting can create a new recording when the EPG programme changes. The timing preference helps place the split around the programme boundary. This makes longer viewing sessions easier to browse later as individual programmes instead of one continuous recording.

Programme information gives the recording collection a more meaningful structure than a list of unexplained files. It helps connect retained material with what the viewer actually watched.

## Choose a convenient destination

The setup screen lets users choose the movie folder, including available local and network storage. A CIFS mount watchdog attempts to restore a dropped network movie folder. This is useful when the receiver normally saves to a NAS rather than its internal disk.

Destination choices matter when the receiver is part of a wider home setup. The viewer can use the supported storage arrangement that fits how recordings will later be accessed.

## Manage storage deliberately

Settings include cleanup timing, removal of old leftover buffers and a low-free-space threshold. These controls help fit automatic recording around the receiver's storage. The reviewed version also displays a setting for keeping only the newest number of autosaves, but that count limit is currently inactive; saved recordings still need deliberate storage management.

Storage controls make the recording habit easier to maintain over time. Review retention choices alongside the available destination so the collection remains useful instead of simply growing without attention.

## Set it up from the receiver

The plugin provides an on-screen setup and About view, with save and cancel actions using the receiver's normal remote-control workflow. It is intended for OpenPLi receivers with a working live buffer; the project's documented tested setup is OpenPLi 9.2 on a VU+ Duo4K SE. A disk or NAS must have enough free space and remain available for saving.

The receiver-side settings keep the feature close to the viewing routine. Adjust the supported choices there rather than maintaining an unrelated desktop workflow.


---

Project repository: [le-auto-record](https://github.com/logicencoder/le-auto-record)

See [REPOS.md](REPOS.md) for the project links.

**[Logic Encoder](https://logicencoder.com)** · [GitHub](https://github.com/logicencoder) · [Contact](https://logicencoder.com/contact/)
