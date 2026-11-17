# Outlet Check

Eight quick checks that show what a restaurant outlet needs next: marketing, or something to sort out first, such as margins, monthly bills, the guest experience, value for money or cash. It works for dine-in restaurants, cafés and quick-service outlets, with or without delivery, and for delivery-only kitchens (enter 0 seats and the dining-room check is skipped).

A one-page app with no server and no database. Numbers are saved only in the browser of the phone or laptop that typed them. One device can keep several outlets: pick one, rename it or add another from the **Outlet** box at the top.

Files: `index.html` (the app), `manifest.json`, `sw.js` and the icons (these let it install on a phone and open offline).

## Put it online for free

### Option A: GitHub Pages (simplest)

1. On github.com, create a new repository, for example `outlet-check`. On the free plan it has to be **public**. The code is public, but nobody's numbers are in it.
2. Upload every file in this folder to the top level of the repository.
3. Open **Settings → Pages**. Under Source choose **Deploy from a branch**, pick **main** and **/ (root)**, then Save.
4. About a minute later the app is live at `https://<your-username>.github.io/outlet-check/`.

### Option B: Cloudflare Pages (keeps the code private)

1. In the Cloudflare dashboard open **Workers & Pages → Create → Pages → Upload assets**.
2. Name the project, drag this folder in, and deploy.
3. The app is live at `https://<project-name>.pages.dev`.

### Your own address (optional)

To use an address like `check.example.com`, add the domain in the host's custom-domain settings and create the DNS record it asks for (usually a CNAME) where the domain is managed.

## Updating the app

1. Replace `index.html` with the new version.
2. In the first lines of `sw.js`, raise the version number by one (for example `outlet-check-v2` becomes `outlet-check-v3`). Installed phones then pick up the new version the next time they open it online.

## Privacy

- Each person's numbers stay in their own browser. Two owners on two phones do not see each other's entries. Use **Copy summary** or **History → Download backup** to share or keep them.
- Clearing browser data deletes the numbers. Download a backup now and then. One backup file holds every outlet on the device, and restoring it never removes outlets that are already there.
- The page tells search engines not to list it. Anyone with the link can still open it, but they see an empty app with example numbers, not yours.
