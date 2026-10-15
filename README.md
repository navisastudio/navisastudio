# Studio Ledger

A simple dashboard for a working creative: track shoots across every role, keep a rate card, archive designs and CMT forms, and make SST-ready invoices as PDFs (Malaysia, in RM).

**Open it here:** https://YOUR-GITHUB-USERNAME.github.io/studio-ledger/

No sign-up, no install. Open it in Chrome, Edge or Safari on your laptop.

---

## Using it

**Start with Settings.** Add your name, address, phone, email, SST registration number, SSM registration number and TIN (if you have them), bank details and DuitNow ID. These print on every invoice. You can also set your invoice number prefix, SST rate (leave it at 0 if you're not SST-registered), and how many days clients get to pay.

**Rates.** Set your current rate for each role: artist, model, creative director, art director, fashion stylist, fashion designer, set designer, prop rentals. Once you've logged a few jobs, each card shows what you've actually charged (average, range, last time) so you can tell when it's time to raise a rate.

**Jobs.** Add every shoot, past or upcoming. A job can have several roles, one line each. For example: styling, 6 looks, plus creative direction for the day. Choosing a role fills in your current rate. Each job also has space for:
- Brief, deliverables, team and credits, links, and notes
- Call sheets, mood boards, BTS images, and PDFs
- Your own costs on the job (fabric, travel, props hire). These never show on invoices.
- Library items you reused for it

Jobs sort themselves into **Upcoming**, **On now**, and **Past** by their dates.

**Library.** Your archive of designs, CMT forms, mood boards, reference images, and tech packs. CMT forms have fields for fabric, consumption, cutting, making, and trims, plus a total cost to make. Use **Reuse as new** to copy an old design as the starting point for a new one.

**CMT forms (custom garments).** Open a job and click **Start CMT forms**, or open a client and do the same, or add a *CMT form* item in the Library. Pick the client and job, fill in the garment, maker, fabric and costs, and choose which of the four forms to print:
1. Client brief and measurements
2. Design and materials (with the figure page for sketching)
3. Costing and quotation
4. Fitting and alterations (print one copy per fitting)

Details the app already knows (client name and contact, project reference, garment, maker, fabric, costs, event date, your studio contact and payment method) print in blue. Everything else is left blank to fill in by hand. After filling the forms in and attaching swatches or images, scan or photograph each page, then go back to the same item and use **Scanned forms → Add scans**, choosing which form it is. Scans are kept with that client and job, and the Library search finds them by client name.

**Invoices.** Invoices use the Navisa Studio template: the cowhide background, BILLED TO and studio details at the top, a heading such as *SET DESIGN: PROP RENTAL*, then description, price, quantity and total columns, with subtotal, delivery and total, and payment information at the bottom.
- Open a job and click **Create invoice** (lines carry over), click **New invoice** to start blank, or open an old invoice and click **Use as template** to copy it with the next number.
- Add a line per item: description, quantity and price. The role column is optional and only for your own tracking; it never prints.
- Set the heading, the date and optionally a due date (leave due blank to print only the date). The quantity column can read QTY, QTY (M), HOURS, DAYS or PCS.
- Delivery, discount and SST lines appear only when used (delivery always shows, as on the template).
- **Preview** to check it, then **Download PDF** to send it, or **Print**.
- Invoice numbers follow your prefix (for example SD PR 33). Set the prefix and the next number once in Settings.
- For the billed-to block, add the client's company registration number and billing address in Clients.


**Overview.** What's on now, what's next, what you're owed, what's overdue, wrapped jobs you haven't invoiced yet, and which roles earn you the most this year.

### Use it on one device
For now, keep everything on your laptop. Your phone and laptop don't share data, so anything added on your phone won't show up on your laptop. Phone access will come later with cloud sync.

---

## ⚠️ Where your data lives (please read)

Everything is saved **inside the browser on the device you're using**. Nothing is sent to a server, so it stays private, but:

- **Your phone and laptop won't share data.** Pick one main device.
- **Clearing browser data or website data deletes it**, and so does using a private or incognito window.
- **Back up regularly.** Go to Settings → **Download a backup** about every two weeks. It saves one file with everything, images included. Keep it in Google Drive or email it to yourself. The Overview page reminds you when a backup is due.
- **To move to a new device** (or recover), open the link there, go to Settings → **Restore from backup**, and choose the file.

---

## For whoever maintains this

It's a static site: `index.html`, `vendor/jspdf.umd.min.js` (PDF generation, MIT license) and `assets/fonts/` (Poppins, used on invoices, SIL Open Font License). There's no build step and no server.

**To host it on GitHub Pages:**
1. Create a public repo named `studio-ledger` and upload these files to its root.
2. Go to repo **Settings → Pages → Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then click **Save**.
3. After a minute or two the site is live at `https://YOUR-GITHUB-USERNAME.github.io/studio-ledger/`. Put that link at the top of this README.

To update it, edit `index.html` and commit. Her data isn't affected, since it lives in her browser, not in the repo.

**Possible next step:** to sync across devices and get automatic cloud backup, add a backend such as Supabase or Firebase (login + database + file storage) in place of the IndexedDB `Store` object in `index.html`.
