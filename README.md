<img src="brand/frs-academy-logo.svg" alt="Future Ready Skills Academy, Two Rivers Schools Network" width="440">

# Two Rivers Future Ready Skills Academy – public preview

A public preview (minimum viable product) of the **Two Rivers Future Ready Skills Academy**, hosted by Southern River College, Western Australia.

The Academy helps teachers bring emerging technology and the Future Ready Skills (Community, Communication, Collaboration, Critical Thinking and Creativity) into classrooms from Foundation to Year 12, and connects schools with industry partners and experts.

**Try it:** open the site and use **Try as** (top right) to see the Academy as a Teacher, School Leader, Industry Partner, Expert, Invited visitor or Admin. **Then tell us what you think:** the **📝 Take the 6-minute survey** button opens a short Microsoft Forms survey.

- **Sample data only.** Nothing you type is saved or sent anywhere, no emails are sent, and reloading resets everything. Names marked "(demo)" or "Sample:" are not real people or organisations.
- The live Academy, with real accounts and data, runs separately. This repository holds no personal information, access rules or operational settings.

## What's in this repository

| Path | What it is |
| --- | --- |
| `index.html` | The preview (the whole app in one file), with the survey button |
| `survey/index.html` | The student survey page for surveys on students' own devices (opens at `/survey`) |
| `staff/` | The staff presentation: 17 slide pictures, the PDF and the PowerPoint |
| `brand/`, `favicon.ico` | The Academy logo files, browser and home-screen icons, and the image shown when the link is shared |
| `video/` | The one-minute introduction video shown at the top of the welcome page, and its poster image |
| `vercel.json` | Vercel settings: clean URLs, security headers, no search-engine indexing |
| `robots.txt` | Asks search engines not to list the preview |

It is a static site: there is no build step and no server code. These files are generated from the private portal repository (`npm run build:public`); make changes there, not here.

## Publish on Vercel

1. In Vercel, choose **Add New… › Project** and **Import** this repository.
2. Framework Preset: **Other**. Leave Build Command and Output Directory empty. Press **Deploy**.
3. To update, replace the files in this repository with a new `dist/public` from the portal repository and commit. Vercel redeploys within a minute.

Search engines are asked not to list the site (`noindex`), so it is shared by link or QR code. To let search engines find it, remove the `X-Robots-Tag` header from `vercel.json`, the robots meta tag from `index.html`, and `Disallow: /` from `robots.txt`.

## Outside requests

The preview loads Google Fonts, and when needed the PowerPoint library (cdn.jsdelivr.net), the spreadsheet library (cdnjs.cloudflare.com) and the QR scanner library. Resource links open the FRS materials on Google Drive and Canva, and the survey opens in Microsoft Forms.

## Copyright

All contents, © Government of Western Australia 2026, unless otherwise stated ([education.wa.edu.au/copyright](https://www.education.wa.edu.au/copyright)). FRS resources © Department of Education WA 2024 (frs.srczone.net). This repository is shared for review; it is not licensed for reuse.
