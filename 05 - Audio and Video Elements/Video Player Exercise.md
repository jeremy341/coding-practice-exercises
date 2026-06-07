The `video` element is used to embed video content, such as clips, movies, or advertisements, directly into a webpage.

Like the `audio` element, the `video` element supports several attributes to control media playback, dimensions, and visual presentation.

Below is an example of an HTML page that sets up a responsive video player with multiple fallback formats and a custom cover image. Enable the interactive editor to view the page preview. Try removing the `muted` attribute or changing the `width` value to see how the player behaves in the preview window.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Working with the HTML Video Element</title>
</head>
<body>
  <h1>Working with the HTML Video Element</h1>
  <video
    width="640"
    loop
    controls
    muted
    poster="https://cdn.freecodecamp.org/curriculum/labs/past-event2.jpg"
  >
    <source
      src="https://cdn.freecodecamp.org/curriculum/labs/what-is-the-map-method-and-how-does-it-work.mp4"
      type="video/mp4"
    >
    <source
      src="https://cdn.freecodecamp.org/curriculum/labs/mapmethod.webm"
      type="video/webm"
    >
    <source
      src="https://cdn.freecodecamp.org/curriculum/labs/mapmethod.ogg"
      type="video/ogg"
    >
    <source
      src="https://cdn.freecodecamp.org/curriculum/labs/mapmethod.mov"
      type="video/quicktime"
    >
  </video>
</body>
</html>
```

Let's break down the key attributes and elements used to configure this video player:

### Video Player Attributes

#### 1. `width` (and `height`)
Specifies the dimensions of the video player in pixels.
```html
<video width="640" height="360"></video>
```
Setting width and height prevents the layout from shifting or jumping while the video is loading.

#### 2. `controls`
Similar to the audio player, you must include the `controls` attribute to display the browser's default user interface, which includes play, pause, volume, scrubbing, and fullscreen toggles.
```html
<video controls></video>
```

#### 3. `loop`
A boolean attribute that automatically restarts the video from the beginning once it reaches the end.
```html
<video loop controls></video>
```

#### 4. `muted`
A boolean attribute that mutes the video's audio by default when the page loads.
```html
<video muted controls></video>
```
> [!NOTE]
> Modern web browsers often block videos from autoplaying unless the `muted` attribute is present. If you want a video to play automatically when a user visits your site, you should use `autoplay muted`.

#### 5. `poster`
Specifies the URL of an image to be shown as a placeholder while the video is downloading, or until the user clicks the play button.
```html
<video poster="placeholder-image.jpg" controls></video>
```
If no poster is specified, the browser will typically display the first frame of the video once it is available.

---

### Supporting Multiple Formats with the `source` Element
Web browsers support different video codecs and formats. By nesting `<source>` elements inside the `<video>` element, you can provide options like MP4, WebM, Ogg, and QuickTime:

```html
<video controls>
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
  Your browser does not support the video element.
</video>
```

* The browser reads the sources from top to bottom and plays the first format it is compatible with.
* The `type` attribute specifies the MIME type of the video file, helping the browser determine if it can play the file without downloading it first.
* The text inside the `<video>` element acts as fallback content for older browsers.

Understanding how to combine these attributes will help you build reliable, accessible, and high-performance video players in your web applications.