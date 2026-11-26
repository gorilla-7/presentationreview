# Imported static website

- The user requested publishing the imported `index.html` unchanged, despite its lack of visible page content and broken relative redirect. Do not change that file as part of setup.
- Use the **Preview website** workflow to run `python3 -m http.server 5000 --bind 0.0.0.0`.
- Publishing is configured as a static site with the project root (`.`) as the public directory; no build step is needed.
- The user must click Publish to make the site public.
- The existing script redirects to `www.google.com` plus the URL fragment without an HTTPS scheme. Browsers interpret this as a local path, so visitors may encounter a missing-page error. This behavior was intentionally preserved at the user's request.
