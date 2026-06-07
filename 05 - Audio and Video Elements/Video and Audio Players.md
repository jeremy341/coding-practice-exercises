In web development, you will often need to display different kinds of media on the same webpage. You can combine HTML's `audio` and `video` elements to create a rich multimedia experience. Organizing these different media players using semantic elements like `section` is a best practice that improves both site structure and accessibility.

Below is an example of an HTML page that features both a video lesson and an audio track side by side. Enable the interactive editor to view the page preview. Try adding or removing semantic sections, or changing the text in the headings to see how it affects the preview.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>HTML Audio and Video Lab</title>
  </head>
  <body>
    <h1>HTML Audio and Video Lab</h1>
    <section>
      <h2>What is the map method and how does it work?</h2>
      <video controls width="640">
        <source src="https://cdn.freecodecamp.org/curriculum/labs/what-is-the-map-method-and-how-does-it-work.mp4" type="video/mp4"/>
      </video>
    </section>
    <section>
      <h2>Driving Away</h2>
      <audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/we-are-going-to-make-it.mp3" controls loop>   
      </audio>
    </section>
  </body>
</html>
```

Let's look at the key concepts and structures introduced in this lab:

### Semantic Page Structure
We use the `section` element to divide the webpage into distinct thematic areas:
* The first `section` groups the video player and its related title.
* The second `section` groups the audio player and its related title.

Using semantic elements like `section` helps web browsers, screen readers, and search engines understand the outline and layout of your page content.

---

### Combining Media Elements

#### 1. The Video Section
The video player uses a nested `source` element to supply the video track:
```html
<video controls width="640">
  <source src="video-file.mp4" type="video/mp4"/>
</video>
```
* The `controls` attribute displays play, pause, volume, and fullscreen controls.
* The `width="640"` attribute ensures the player is sized correctly.
* The nested `source` element points to the `.mp4` file and specifies its MIME type (`type="video/mp4"`).

#### 2. The Audio Section
The audio player is configured to automatically repeat and play background music:
```html
<audio src="music-file.mp3" controls loop></audio>
```
* The `src` attribute specifies the URL or file path of the audio resource directly on the `audio` tag.
* The `controls` attribute displays play, pause, seek, and volume buttons.
* The `loop` attribute ensures the music starts over automatically when it finishes.

Using these elements in combination allows you to build sophisticated portfolio pages, learning dashboards, or landing pages featuring interactive audio and video content.