ZP12 local sample editor — compatibility build
================================================


This is a local copy of the ZP12 sample editor from the supplied repository.


Change made

:The original editor only accepted Web MIDI port names containing "felucca".
ZP12 2.5 documents its USB audio/MIDI device name as "zp12 FM-1".
The detector now accepts either "felucca" (legacy firmware) or "zp12 FM-1"
(ZP12 2.5), while still ignoring disconnected ports.

No sample-transfer protocol code was changed.


Run it
------

1. Extract this folder.

2. Open a terminal in this folder.

3. Run:  python -m http.server 8000

4. In Chrome or Edge, open: http://localhost:8000/

5. Connect the FM-1 by USB, close other MIDI applications, and press Connect.


Notes
-----
- Web MIDI with SysEx is required; use desktop Chrome or Edge.
- The browser will ask for MIDI access.
- This is a compatibility patch, not a hardware-verified test. The FM-1
  must be connected to verify the complete handshake and sample transfer.
- The editor is GPL-3.0-only. See the upstream repository for the full
  license and attribution: https://github.com/zvenson/zp12
