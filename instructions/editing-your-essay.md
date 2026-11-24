---
title: Editing Your Essay
layout: base
header-image: "/assets/images/immigration_collage.jpg"
header-tier: banner
header-title: Editing Your Essay
header-position: 35% center
---

{% include nav/instructions-tabs.html active="editing" %}

# How to edit your essay

This page shows you how to change the words, headings, images, and audio in your essay. Everything happens in your web browser. You do not need to install anything.

If you have not made your essay folder yet, do the **Publish your story** tab first.

## Before you start: open your essay

1. Go to your copy of the project on GitHub and sign in.
2. Open the editor in one of two ways:
   - Press the **period key (`.`)** on your keyboard. A code editor opens in a new browser tab.
   - If the period key doesn't work, look at the web address at the top of your browser. Change `github.com` to `github.dev` and press **Enter**. For example, `https://github.com/your-name/MigrationStories` becomes `https://github.dev/your-name/MigrationStories`.

![The editor open in the browser, with the web address at the top and the files listed on the left]({{ '/assets/images/instructions/open-repo.png' | relative_url }})
3. On the left, click the **`essays`** folder, then your own folder, then **`index.md`**. Your essay opens in the middle of the screen.

![The file list with essays, then your folder, then index.md highlighted]({{ '/assets/images/instructions/open-essay.png' | relative_url }})

You can click anywhere in the text and type, just like in a word processor.

> **Always check you are in your own folder.** Before you change anything, look at the file path at the top of the editor, or the open folder in the left list. It should say `essays/your-name/index.md` with your own name. Never edit the `template` folder or a classmate's folder.

## Get back to your repository

If you want to leave the editor and return to your project on GitHub:

1. Click the **three horizontal lines** (the hamburger menu) in the top left corner of the editor.
2. Choose **Go to Repository**. Your project page opens on GitHub.

## The top of your essay (the front matter)

The first lines of `index.md`, between the two rows of dashes (`---`), are called the **front matter**. This is where your title, name, and main image are set. Everything below the second row of dashes is the body of your essay.

![The front matter at the top of index.md]({{ '/assets/images/instructions/front-matter.png' | relative_url }})

**Do not change or delete any quotation marks (`"`) that are already there.** Type your words between them. If a quotation mark disappears, your page can break.

```
---
title: "Your title"
student: "Your name"
lead-image: images/my-photo.jpg
---
```

## Edit text

1. Click in the paragraph you want to change.
2. Select the old words with your mouse and type your own over them.
3. Press **Ctrl+S** (**Cmd+S** on a Mac) to save.

![A paragraph selected and ready to type over]({{ '/assets/images/instructions/edit-text.png' | relative_url }})

Things to keep in mind:

- Leave a blank line between paragraphs. If you don't, they will run together.
- To make a word *italic*, put one star on each side: `*word*`. For **bold**, put two stars on each side: `**word**`.
- Do not delete blocks that start with `{% raw %}{% include{% endraw %}` and end with `{% raw %}%}{% endraw %}`. Those are your images and audio. The next sections show how to change them.

## Edit headings and subtitles

Headings are the lines that start with `#` marks.

```
## Subheader 1: The Journey
```

1. Find the heading line.
2. Change only the words after the `##` and the space. Keep the two `#` marks.

![A heading line selected, with the two # marks circled to keep]({{ '/assets/images/instructions/edit-heading.png' | relative_url }})
3. Save with **Ctrl+S**.

A heading must have a space after the `#` marks. `##Journey` will not work, but `## Journey` will.

To change your **main title**, edit the `title:` line in the front matter instead. Keep the quotation marks around it.

## Add the main image (front matter)

This is the large image at the top of your essay.

1. In the left file list, open your folder. Right-click the **`images`** folder and choose **Upload...**.
2. Choose your picture from your computer. It will appear inside `images`.

![Right-clicking the images folder with Upload highlighted]({{ '/assets/images/instructions/upload-image.png' | relative_url }})
3. In the front matter, change the three image lines:

```
lead-image: images/my-photo.jpg
lead-image-alt: "A short description of what is in the picture"
lead-image-caption: "Who is in it, where, when, and where the picture came from."
```

4. Type the file name exactly as it appears in the `images` folder, including capital letters and the ending (`.jpg`, `.png`).

![The three lead-image lines filled in, with the matching file in the images folder]({{ '/assets/images/instructions/lead-image.png' | relative_url }})
5. Save.

Tips: use lowercase names with dashes and no spaces (`grandmothers-suitcase.jpg`). The "alt" line is for people who can't see the image, so describe what it shows.

## Add an image inside your essay

1. Upload the picture into your `images` folder, the same way as above.
2. In `index.md`, click on an empty line where you want the picture to appear. Leave a blank line above and below it.
3. Paste this block and change the three parts inside the quotation marks:

```
{% raw %}{% include essay/figure.html
  image="images/my-photo.jpg"
  alt="Short description of the picture"
  caption="What it shows and where it came from."
%}{% endraw %}
```

4. Save.

![An image block in the essay with the image path circled]({{ '/assets/images/instructions/include-image.png' | relative_url }})

To change a picture that is already there, change only the file name after `image=`. To make it bigger or smaller, add a line `size="small"` or `size="large"` before the `%}`.

## Add audio

1. Make sure your clip is an **MP3** file.
2. Right-click the **`audio`** folder inside your essay folder and choose **Upload...**. Pick your MP3.

![Right-clicking the audio folder with Upload highlighted]({{ '/assets/images/instructions/upload-audio.png' | relative_url }})
3. In `index.md`, find the audio block (it starts with `{% raw %}{% include essay/audio.html{% endraw %}`) or paste this where you want the clip:

```
{% raw %}{% include essay/audio.html
  file="audio/my-clip.mp3"
  caption="Who is speaking, what they describe, and your citation."
%}{% endraw %}
```

4. Change `my-clip.mp3` to the exact name of your file.
5. Write your caption, then save.

![The audio block with the MP3 file name filled in]({{ '/assets/images/instructions/add-audio.png' | relative_url }})

## Save your work and put it on the website

Saving with Ctrl+S only saves it in your browser. To publish your changes:

1. Click the **Source Control** icon on the left (it looks like three dots connected by lines).
2. Type a short message in the box, like "Edit my essay".
3. Click **Commit & Push** (or the checkmark). If it asks whether to stage changes, choose **Yes**.

![The Source Control icon, message box, and Commit and Push button]({{ '/assets/images/instructions/commit-change.png' | relative_url }})
4. Wait a few minutes, then follow the steps below to check that your change went live.

## Watch your change build (Actions tab)

1. Go back to your repository (hamburger menu, then **Go to Repository**).
2. Click the **Actions** tab near the top.
3. Click the newest item in the list. It matches your commit message.
4. Look at the icon next to it: a yellow circle means it is still building, a green check means it worked, and a red X means something went wrong. Building usually takes a few minutes.
5. If you see a red X, check your quotation marks and file names, then commit again. Ask your instructor if it keeps failing.

![The Actions tab with a green check next to the latest run]({{ '/assets/images/instructions/view-website-building.png' | relative_url }})

## Check your changes on your site

1. Once the Actions item has a green check, open your website. The address is usually `https://your-github-username.github.io/MigrationStories/`.
2. Click **Essays** and open your essay.
3. Reload the page (**Ctrl+R**, or **Cmd+R** on a Mac). If you still see the old version, hold **Shift** while you reload.
4. Read through your essay. Check the text, headings, images, and that the audio plays.

## If something goes wrong

- **A picture or audio clip doesn't show.** The file name doesn't match. Check capital letters, dashes, and the ending.
- **The page looks broken.** Check that the quotation marks in the front matter are still there and that both rows of dashes (`---`) are still in place.
- **You made a mistake.** Press **Ctrl+Z** to undo.
- Still stuck? Ask your instructor and tell them which step you were on.
