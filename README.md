# Yardsmith - Landing Page

A single self-contained landing page for Yardsmith. All images are embedded
directly in `index.html` as base64 data, so there are no separate asset
folders and nothing else to upload.

## Files

- `index.html` - the entire site (markup, styles, script, images, all in one file)
- `vercel.json` - minimal Vercel configuration for a static site
- `.gitignore` - keeps local editor/OS files out of the repository

## 1. Push this folder to GitHub

```bash
cd yardsmith-deploy
git init
git add .
git commit -m "Yardsmith landing page"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

If you would rather not use the command line, you can also create a new
repository on github.com and use "Add file - Upload files" to drag in
`index.html`, `vercel.json` and `.gitignore` directly from this folder.

## 2. Deploy on Vercel

1. Go to vercel.com and sign in (GitHub login is the fastest option).
2. Click **Add New - Project**.
3. Select the GitHub repository you just pushed.
4. Framework preset: choose **Other** (this is a plain static HTML site,
   no build step needed).
5. Leave the build and output settings empty and click **Deploy**.

Vercel will give you a live `.vercel.app` URL immediately. You can later
attach a custom domain (for example `yardsmith.app`) from the project's
**Settings - Domains** tab.

Every time you push a new commit to the `main` branch, Vercel will
automatically redeploy the site.

## 3. Activate the contact form (one-time step)

The "Request a Free Demo" / "For Investors" buttons open a form that sends
submissions straight to **kseniia.kklsh@gmail.com** using a free service
called FormSubmit, no backend or account required.

The very first submission ever sent will trigger a one-time confirmation
email from FormSubmit to that address. Click the confirmation link in that
email once, and every submission after that will arrive automatically.
Until that link is clicked, submissions will appear to send successfully
in the browser but will not actually be delivered.

## Making changes later

Everything lives in `index.html`. To update text, colors, or images, edit
that file directly and push the change to GitHub. Vercel will redeploy
automatically. Images are embedded as base64, so if you want to replace one,
it needs to be re-encoded and pasted back into the relevant `src="data:image/..."`
attribute, or ask Claude to do this for you.
