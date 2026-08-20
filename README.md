# Process sign-off — trial

A single-page form for signing off production stages from a phone. Scan the QR
code on the tracker sheet, type the job number, pick the process, sign, send.

- `index.html` — the form
- `qr.html` — makes the printable QR label

Hosted with GitHub Pages, emailed via Web3Forms. No build step, no dependencies.

## Setting it up

1. **Web3Forms key.** Go to web3forms.com, enter the inbox that should receive
   sign-offs, and it emails you an access key. Open `index.html`, find
   `WEB3FORMS_KEY: ""` near the bottom and paste the key between the quotes.
2. **Publish.** Settings → Pages → Deploy from a branch → `main` / `/ (root)`.
   The site appears at `https://USERNAME.github.io/REPO/` in a minute or two.
3. **QR code.** Open `qr.html` on the published site, paste in the address of
   `index.html`, download the PNG and drop it onto the tracker template.

Until a key is set the form runs in sample mode: it shows the email it would
send and hands it to the phone's mail app instead.

## Settings

Everything adjustable is in one `CONFIG` block at the bottom of `index.html`:
the Web3Forms key, the email domain, the manager, the process list, the sales
rep list, and the job-number lookup table.

## Free plan limits

250 submissions a month, one recipient per key, no attachments — the signature
is captured and shown on screen but is not attached to the email.
