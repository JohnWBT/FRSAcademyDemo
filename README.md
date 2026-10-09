# Two Rivers Future Ready Skills Academy – review demo

A standalone review demo of the Two Rivers Future Ready Skills Academy app, hosted by Southern River College.
It uses **sample data only**: nothing is saved, no emails are sent, and reloading resets everything.
Use **Try as** (top right) to switch between Teacher, School Leader, Industry Partner, Expert, Invited visitor and Admin.

## What's in this repository

| Path | What it is |
| --- | --- |
| `index.html` | The review demo (the whole app in one file) |
| `survey/index.html` | The student survey page for surveys on students' own devices (opens at `/survey`) |
| `staff/` | The staff presentation: 17 slide pictures, the PDF and the PowerPoint |
| `vercel.json` | Vercel settings: clean URLs, security headers, no search-engine indexing |
| `robots.txt` | Asks search engines not to list the demo |

It is a static site: there is no build step and no server code.

## Publish on Vercel

1. **Create the repository.** On GitHub, choose **New repository** (for example `frs-academy-demo`; private is fine). Choose **uploading an existing file**, drag in everything from this folder, including the `staff` and `survey` folders, and press **Commit changes**.
2. **Import it into Vercel.** In Vercel, choose **Add New… › Project**, connect GitHub if asked, and **Import** the repository.
3. **Settings.** Framework Preset: **Other**. Leave Build Command and Output Directory empty (the root folder is the site). Press **Deploy**.
4. **Open the link** Vercel gives you (for example `frs-academy-demo.vercel.app`). The student survey page is at `/survey`, and the demo's class codes and QR codes point there automatically.

**Updating:** replace `index.html` (and `staff/` or `survey/index.html` if they changed) in GitHub. Vercel redeploys within a minute.

**Your own address (optional):** in Vercel, **Settings › Domains**, add for example `demo.frs.srczone.net`, then add the CNAME record Vercel shows to the srczone.net DNS.

## Notes

- The demo sends nothing anywhere. The only outside requests are Google Fonts, the PowerPoint library (cdn.jsdelivr.net, when a slide deck is downloaded), the spreadsheet library (cdnjs.cloudflare.com, for Excel downloads), the QR scanner library (when a camera scan is used) and links to the FRS resources on Google Drive and Canva.
- Names marked "(demo)" or "Sample:" are not real people or organisations.
- The live Academy, with real accounts and data, runs separately; this repository holds no personal information.

All contents, © Government of Western Australia 2026, unless otherwise stated ([education.wa.edu.au/copyright](https://www.education.wa.edu.au/copyright)). FRS resources © Department of Education WA 2024 (frs.srczone.net).
