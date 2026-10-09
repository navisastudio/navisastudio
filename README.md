# Studio Ledger

A simple dashboard for a working creative: track shoots across every role, keep a rate card, archive designs and CMT forms, and make GST invoices as PDFs.

**Open it here:** https://navisastudio.github.io

No sign-up, no install. It works on a laptop or a phone.

---

## Using it

**Start with Settings.** Add your name, address, phone, email, GSTIN and PAN (if you have them), bank details and UPI ID. These print on every invoice. You can also set your invoice number prefix, GST rate, and how many days clients get to pay.

**Rates.** Set your current rate for each role: artist, model, creative director, art director, fashion stylist, fashion designer, set designer, prop rentals. Once you've logged a few jobs, each card shows what you've actually charged (average, range, last time) so you can tell when it's time to raise a rate.

**Jobs.** Add every shoot, past or upcoming. A job can have several roles, one line each. For example: styling, 6 looks, plus creative direction for the day. Choosing a role fills in your current rate. Each job also has space for:
- Brief, deliverables, team and credits, links, and notes
- Call sheets, mood boards, BTS images, and PDFs
- Your own costs on the job (fabric, travel, props hire). These never show on invoices.
- Library items you reused for it

Jobs sort themselves into **Upcoming**, **On now**, and **Past** by their dates.

**Library.** Your archive of designs, CMT forms, mood boards, reference images, and tech packs. CMT forms have fields for fabric, consumption, cutting, making, and trims, plus a total cost to make. Use **Reuse as new** to copy an old design as the starting point for a new one.

**Invoices.** Open a job and tap **Create invoice**. The lines carry over. Add a discount, GST (shown as CGST + SGST, or IGST), and any advance received, then **Download PDF**. Change the status to Sent, Partly paid, or Paid as money comes in.

**Overview.** What's on now, what's next, what you're owed, what's overdue, wrapped jobs you haven't invoiced yet, and which roles earn you the most this financial year.

### On your phone
Open the link, then:
- **iPhone (Safari):** Share → Add to Home Screen
- **Android (Chrome):** ⋮ menu → Add to Home screen

It then opens like an app.

---

## Where your data lives (please read)

Everything is saved **inside the browser on the device you're using**. Nothing is sent to a server, so it stays private, but:

- **Your phone and laptop won't share data.** Pick one main device.
- **Clearing browser data or website data deletes it**, and so does using a private or incognito window.
- **Back up regularly.** Go to Settings → **Download a backup** about every two weeks. It saves one file with everything, images included. Keep it in Google Drive or email it to yourself. The Overview page reminds you when a backup is due.
- **To move to a new device** (or recover), open the link there, go to Settings → **Restore from backup**, and choose the file.

---

## For whoever maintains this

It's a static site: `index.html` plus `vendor/jspdf.umd.min.js` (PDF generation, MIT license). There's no build step and no server.

**To host it on GitHub Pages:**


To update it, edit `index.html` and commit. Her data isn't affected, since it lives in her browser, not in the repo.

**Possible next step:** to sync across devices and get automatic cloud backup, add a backend such as Supabase or Firebase (login + database + file storage) in place of the IndexedDB `Store` object in `index.html`.
