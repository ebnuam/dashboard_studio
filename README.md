# Kok Iso Yo? — Studio Dashboard (Cloudflare Pages)

Frontend kontrol produksi video dokumenter **Kok Iso Yo?** berbasis Remotion + Three.js (`dashboard_studio`) yang di-host statis di **Cloudflare Pages** dan terhubung ke backend VPS melalui **Cloudflare Tunnel**.

## Fitur
- **Video & Download:** Streaming vertikal `9:16` (`HTTP 206 Partial Content`) + Download `.mp4` + ringkasan QA `short_qa.py`.
- **Live tmux & Log:** Pemantauan progres frame render aktif & log VPS real-time.
- **QA Sheets & Naskah:** Viewer *contact sheet* resolusi penuh, transkrip, *storyboard*, & catatan cek fakta.
- **Prompt & Upload Audio:** Penyimpanan brief/prompt episode + upload `.mp3`/`.wav`/`.m4a` beserta deteksi jeda otomatis (`ffprobe` + `silencedetect`).
- **Render & Revisi:** Pemicu render *QA stills*, *selective frame-range patch*, render penuh di `tmux`, serta catatan revisi.

## Deploy di Cloudflare Pages
1. Buka **Cloudflare Dashboard → Workers & Pages → Create → Pages → Connect to Git**.
2. Pilih repository **`ebnuam/dashboard_studio`** (branch `main`).
3. **Build command:** *(kosongkan)* | **Build output directory:** `/` (root).
4. Setelah URL `*.pages.dev` aktif, buka web-nya → isi **URL API VPS** (mis. URL Cloudflare Tunnel `https://...`) dan **PIN Studio**.
   *(Tip: bisa juga langsung lewat query URL `?api=https://...`)*
