# Payhip delivery package — build instructions

**Product:** Markdown Importer for Adobe InDesign and Illustrator  
**Version:** 1.6.0  
**Target ZIP name:** `MD-Importer-Full-1.6.0.zip`

---

## Folder layout (before ZIP)

```text
release/payhip/MD-Importer-Full-1.6.0/
├── README.md
├── manual.md
├── MD-Importer.jsx              ← copy from standalone/MD-Importer.jsx
├── MD-Importer-1.6.0.zxp        ← you build & sign (see meta/ZXP_PACKAGING.md)
└── samples/
    └── demo.md
```

---

## 1. Update standalone copy

After code changes, refresh the buyer copy:

```powershell
Copy-Item -Force "standalone\MD-Importer.jsx" "release\payhip\MD-Importer-Full-1.6.0\MD-Importer.jsx"
```

---

## 2. Build ZXP (your step)

Pack the CEP extension per `meta/ZXP_PACKAGING.md`:

- `CSXS/manifest.xml`
- `index.html`, `css/`, `js/`, `jsx/MD-Importer-host.jsx`
- `standalone/MD-Importer.jsx` (inside the bundle)

Sign with your certificate, save as:

`release/payhip/MD-Importer-Full-1.6.0/MD-Importer-1.6.0.zxp`

Test: clean install → **Window → Extensions → MD Importer** → import `samples/demo.md`.

---

## 3. Create Payhip ZIP

```powershell
cd "release\payhip"
Compress-Archive -Path "MD-Importer-Full-1.6.0\*" -DestinationPath "MD-Importer-Full-1.6.0.zip" -Force
```

Upload `MD-Importer-Full-1.6.0.zip` to Payhip as the digital download.

**Payhip listing text:** copy from `PAYHIP-DESCRIPTION.txt` (includes YouTube: https://youtu.be/qtHSx2Y0sso).

**YouTube:** paste `YOUTUBE-DESCRIPTION.txt` into the video description; pin `YOUTUBE-PINNED-COMMENT.txt` as a comment.

---

## 4. Smoke test (recommended)

On a machine without the dev extension folder:

1. Unzip the delivery archive.
2. Install `MD-Importer-1.6.0.zxp` (ZXP Installer / Anastasiy).
3. Open InDesign → panel → Import `samples/demo.md`.
4. Repeat in Illustrator (expect host-specific limits — see `manual.md`).
5. Run `MD-Importer.jsx` via **File → Scripts → Other Script…** (standalone path).

---

## Do not include in Payhip ZIP

- `meta/`, `.git/`, signing keys (`.pem`, `.p12`)
- Demo jsxbin (`MD-Importer-Demo.jsx`)
- Unsigned or debug-only CEP folders
