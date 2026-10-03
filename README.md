# Freelancer invoice

A single-page invoice you fill in in the browser. The preview updates as you type. Totals are in US dollars. The last draft stays in this browser (`localStorage`); a refresh does not clear it. No account, server, or internet connection is required.

## Open it

Double-click `index.html`, or from this folder run:

```bash
python3 -m http.server 8765
```

Then open http://localhost:8765 . Either way works. The first visit loads an obvious example (Example Studio / Sample Client LLC). Replace the fields with your own. Use **Add line** and the × on a row for line items. Tax percent is optional; leave it blank for no tax.

**Save as PDF** opens the browser print dialog. Choose “Save as PDF” (or Microsoft Print to PDF). The form is hidden; only the invoice prints. For a cleaner page, turn off headers and footers in the print dialog. **Reset example** puts the sample invoice back (it asks first).

Drafts are stored only in this browser on this device, under the key `freelancer-invoice-draft-v1`. Clearing site data removes them. Do not put real client details into a public copy of the file if you change the built-in example.

## Publish it

The folder is static: `index.html` plus this readme. Host the folder as-is.

- **Netlify:** Netlify Drop, or a site whose publish directory is this folder. No build command.
- **GitHub Pages:** push the folder to a repository and set Pages to serve the branch (root, or `/docs` if you move the files there).
- **Any static host** (Cloudflare Pages, Amazon S3, a web server) works the same way. Open the site over HTTPS so each visitor’s draft stays private to their own browser.

Nothing here signs people in or sends invoices. Publishing only hosts the page; each visitor’s data remains on their machine.
