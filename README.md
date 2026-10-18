# SidMade Portfolio

Portfolio website of **Siddharthar A**, a creative designer and visual editor working under **SidMade** (graphic design, video editing and photo editing).

Plain HTML, CSS and a little JavaScript in a single `index.html`. No frameworks, no build step, no dependencies to install.

## What is on the site

- **Landing:** introduction, brand line and two actions (Explore My Work, Let's Work Together).
- **Poster showcase:** two rows of posters that slide sideways as you scroll.
- **Services:** Graphic Design, Video Editing, Photo Editing.
- **Selected Work:** three poster series cards. Click a poster to open the viewer, then use the arrow buttons, the keyboard left and right arrow keys, or swipe on a phone to move between posters. Escape closes it.
- **Start a Project:** opens a small box with two direct options, a message on Instagram or a ready-to-send email. A "Copy email address" button is included for devices with no mail app.
- **Contact:** the same two options as large buttons.
- **Light and dark themes:** a switch in the top bar. It follows the device setting first and remembers the visitor's choice. The Services block always contrasts with the page (white on dark, black on light).
- **Responsive:** the layout adapts to phones, tablets and desktops.
- **Accessibility:** skip link, keyboard navigation, visible focus outlines, labelled buttons, dialog focus handling, and reduced-motion support.

## Folder structure

```
index.html            the whole site (HTML, CSS and JavaScript)
README.md             this file
images/
  photo.jpg           portrait shown in the hero
  posters/
    <name>.jpg        full-size posters, 1000 x 1250 px (used in the viewer)
    sm/<name>.jpg     small posters, 640 x 800 px (used in rows and cards)
```

Poster names in use: `greatest-bw`, `greatest-red`, `greatest-yellow`, `since-1975`, `reintroducing`, `eyes-chico`, `mcgill-wexler`, `santhosh`.

## Publish on GitHub Pages

1. Upload `index.html` and the whole `images` folder to the repository root. Replace the older files if they exist.
2. In the repository open **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select the `main` branch and the `/ (root)` folder, then save.
4. After a minute or two the site is live at `https://<username>.github.io/<repository-name>/`.

All file paths are relative, so the site works under any repository name and under a custom domain.

## How to edit

Open `index.html` in any text editor. The file has three parts: styles at the top, the page content in the middle, and the script at the bottom.

**Change the text:** search for the sentence you want to change and edit it.

**Change contact details:** search for `siddharthararumugam@gmail.com` and `sidmade.in`. The email address appears in the two email links and once in the script (the copy button). The Instagram links are `https://www.instagram.com/sidmade.in/` (profile) and `https://ig.me/m/sidmade.in` (opens a direct message).

**Add a poster:**
1. Save the full poster as `images/posters/<name>.jpg` (about 1000 x 1250 px) and a smaller copy as `images/posters/sm/<name>.jpg` (640 x 800 px). Posters are expected to have a 4:5 shape.
2. Copy an existing poster `<button class="shot" ...>` block inside a series card in `index.html` and change `data-poster`, the image `src` and the description (`alt`).
3. The viewer picks it up automatically.

**Change colours:** edit the values at the top of the `<style>` section, in the `:root` block (light theme) and the two dark blocks right under it. `--red` is the brand red.

**Change fonts:** the site uses two Google Fonts, Archivo Black for headings and Kanit for body text, loaded in the `<link>` tag near the top.

## Adding video and photo work later

The Services section already lists Video Editing and Photo Editing, but Selected Work shows poster designs only. When you have real pieces:
- Add a new series card in the same format as the existing ones, for example "Video Edits" with a link or thumbnail per project, or "Before and After" for photo edits.
- Link videos to Instagram reels, YouTube, or files in a `videos` folder.

## Notes

- All posters shown are personal, fan-made concept designs. This is stated on the site.
- The site does not collect any visitor data and has no tracking or cookies. The only thing it stores in the visitor's browser is the chosen theme.
- Fonts are loaded from Google Fonts. If they are blocked, the site falls back to system fonts.
- The poster rows and the stacked cards use scroll effects. Visitors who have "reduce motion" turned on get the static version.

## Credits

Design, development and posters by Siddharthar A, Coimbatore, India. Copyright 2026 SidMade. All rights reserved.
