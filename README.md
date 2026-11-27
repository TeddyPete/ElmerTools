# ElmerTools: the Ask Elmer apps

Ham radio apps for the [M5Stack CardputerZero](https://docs.m5stack.com/en/CardputerZero),
a pocket Raspberry Pi CM0 Linux handheld with a keyboard and a 320x170 screen.
They carry the **Ask Elmer** brand ([askelmer.com](https://askelmer.com)) and install from
the CardputerZero app store as normal `.deb` apps that launch from the home screen.

| App | Folder | Package | Share code |
| --- | --- | --- | --- |
| Ask Elmer Ham Tools: Antenna Lab (NEC2, 3D pattern, beam optimizer, NanoVNA overlay), band check, RF math, where & when, propagation, satellites, POTA/SOTA, station clock | [`ham-tools/`](ham-tools/) | `askelmer-ham-tools` | AEHT |
| Ask Elmer Ham Exam: study the US license exams with the NCVEC question pools | [`ham-exam/`](ham-exam/) | `askelmer-ham-exam` | AEHX |
| Ask Elmer Morse: Koch trainer, Morse games, paddle keyer, key-out to a radio, CW decoder | [`morse/`](morse/) | `askelmer-morse` | AECW |

Each app lives in its own folder with its own README, tests and `scripts/build_deb.sh`
(`bash ham-tools/scripts/build_deb.sh` writes `ham-tools/build/askelmer-ham-tools_<ver>-1_arm64.deb`).
The 3D-printed key box for the Morse app (paddle in, optocoupler key-out) is in
[`morse/hardware/`](morse/hardware/).

Each app folder is self-contained: it carries its own copy of the shared UI module
(`nomadui.py`, with the standard About screen), the key handling, and the bundled
Barlow Condensed and Atkinson Hyperlegible fonts (SIL OFL). Ham Tools also carries
`nomadgps.py`, the GPS reader that the Ask Elmer and Nomad apps share for time and location.

The AV field apps (Nomad AV Tester, Net Tools, WiFi Share, Packet Capture, Display Control,
AI Bridge) live in [TeddyPete/NomadTools](https://github.com/TeddyPete/NomadTools).
These apps moved here from that repo in November 2026.

## About

Developed by TheTechNomad · [www.TheTechNomad.com](https://www.TheTechNomad.com) ·
[github.com/TeddyPete](https://github.com/TeddyPete)
