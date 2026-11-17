# CLIPMAX

A shorts library website: a 3D glass carousel, a cover grid, and a window with
watch buttons that open YouTube or Instagram.

## Files
- `index.html`  the page (design, animation, sound). You rarely need to touch it.
- `shorts.js`   your content: titles, links and cover images. Edit this one.
- `images/`     put your cover images here (vertical 9:16, JPG, under 300 KB).
- `logo.webp`   the logo, also used as the browser tab icon.

## Add a short
Open `shorts.js` and add a line to `window.SHORTS`:

    { t:'My Short', s:'Action, 0:45', d:'One line about it.',
      yt:'https://www.youtube.com/shorts/VIDEO_ID',
      ig:'https://www.instagram.com/reel/CODE/',
      img:'images/my-short.jpg' },

Leave out `yt` or `ig` if you only have one. Leave out `img` to use generated art.
Use lowercase file names with no spaces, and keep a comma between entries.

## Run it on your computer
Open a terminal in this folder and run:

    python -m http.server 8000

Then open http://localhost:8000. Opening index.html by double-click will not
show your images in the 3D carousel (the browser blocks it).

## Publish on GitHub Pages
Run every command below from INSIDE this folder, so that index.html sits at the top level of the repository.
1. On github.com click New repository, name it `CLIPMAX`, keep it Public, and do not add a README.
2. In this folder run:

       git init
       git add .
       git commit -m "CLIPMAX website"
       git branch -M main
       git remote add origin https://github.com/VENU679/CLIPMAX.git
       git push -u origin main

3. In the repository go to Settings, then Pages. Under Build and deployment choose
   Deploy from a branch, pick `main` and `/ (root)`, then Save.
4. After a minute or two the site is live at https://venu679.github.io/CLIPMAX/

## Update later

    git add .
    git commit -m "Add new shorts"
    git push
