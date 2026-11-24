# Arkvolt Cables - 3D demo website

Single page website for a cable manufacturer with an interactive 3D cable cutaway (Three.js), product switcher, cable size calculator and a 3D factory drum.

## Files

- `index.html` - the whole website (HTML, CSS and JavaScript in one file)
- `.nojekyll` - tells GitHub Pages to serve the files as they are

Three.js r128 and Google Fonts load from public CDNs, so no build step or `npm install` is needed.

## Run locally

Open `index.html` in a browser, or run a small server:

```
python3 -m http.server 8000
```

Then open http://localhost:8000

## Go live on GitHub Pages

1. Create a new public repository on GitHub, for example `arkvolt-cables`.
2. Upload `index.html`, `README.md` and `.nojekyll` to the root of the repository (Add file > Upload files > Commit).
3. Open Settings > Pages.
4. Under "Build and deployment", set Source to "Deploy from a branch", Branch to `main` and folder to `/ (root)`, then Save.
5. After a minute or two the site is live at `https://<your-username>.github.io/arkvolt-cables/`

Using git instead:

```
git init
git add .
git commit -m "Arkvolt Cables 3D website"
git branch -M main
git remote add origin https://github.com/<your-username>/arkvolt-cables.git
git push -u origin main
```

## Where to edit

- Company name, address, phone: search for `Arkvolt` and the contact section near `id="contact"`.
- Stats in the hero: the `.stats` block.
- Cable types and their 3D colours: the `TYPES` object in the script.
- Layer descriptions: the `DESC` object.
- Calculator ratings: the `AMP` table (size in mm², current in A).
- Factory steps: the `STEPS` array.
- The quote form is a demo; connect it to Formspree, Google Forms or your backend before taking real enquiries.
- Remove the "Demo website for a fictional company" line in the footer when real client details go in.
