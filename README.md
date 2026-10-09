# DIVA Mini

Password-gated, single-file viewer of the Abu Dhabi VDV 452/455 (DIVA) exports: Lines & routes, Lines map,
Stops map and Linetrack. No raw tables, no duties, no roster and no driver data.

`index.html` is the password gate with the viewer inside, gzip-compressed and encrypted with AES-256-GCM
(key derived from the password with PBKDF2-SHA256, 300 000 rounds). It is decrypted in the browser; nothing
readable is stored in this repository.

Built by `build/build_viewer.py --mini` in the VDV-DIVA-VIEWER folder of the project workspace
(`build/encrypt_mini.mjs` does the wrapping). Rebuild there and copy `mini/index.html` here to update.
