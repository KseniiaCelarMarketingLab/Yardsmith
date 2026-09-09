# Yardsmith Stables - Landing Page

A single self-contained landing page for Yardsmith Stables. All images and
the logo are embedded directly in `index.html` as base64 data, so there are
no separate asset folders and nothing else to upload.

## Files

- `index.html` - the entire site (markup, styles, script, images, logo, all in one file)
- `vercel.json` - minimal Vercel configuration for a static site
- `.gitignore` - keeps local editor/OS files out of the repository

## 1. Push this folder to GitHub

```bash
cd yardsmith-deploy
git init
git add .
git commit -m "Yardsmith Stables landing page"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

If you would rather not use the command line, create a new repository on
github.com and use "Add file - Upload files" to drag in `index.html`,
`vercel.json` and `.gitignore` directly from this folder.

## 2. Deploy on Vercel

1. Go to vercel.com and sign in (GitHub login is the fastest option).
2. Click **Add New - Project**.
3. Select the GitHub repository you just pushed.
4. Framework preset: choose **Other** (this is a plain static HTML site, no build step needed).
5. Leave the build and output settings empty and click **Deploy**.

Vercel gives you a live `.vercel.app` URL immediately. Attach a custom
domain later from the project's **Settings - Domains** tab. Every push to
`main` triggers an automatic redeploy.

## 3. Activate the contact form (one-time step)

The "Request a Free Demo" / "For Investors" buttons open a form that sends
submissions straight to **kseniia.kklsh@gmail.com** using FormSubmit, a free
service that needs no backend or account.

The very first submission ever sent will trigger a one-time confirmation
email from FormSubmit to that address. Click the confirmation link once,
and every submission after that arrives automatically. Until that link is
clicked, submissions appear to send successfully in the browser but are not
actually delivered.

## Making changes later

Everything lives in `index.html`. To update text, colors, or images, edit
that file directly and push the change to GitHub - Vercel redeploys
automatically. Images and the logo are embedded as base64; to replace one,
it needs to be re-encoded and pasted back into the relevant
`src="data:image/..."` attribute, or ask Claude to do this for you.
