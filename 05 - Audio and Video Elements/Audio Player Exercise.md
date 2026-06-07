The `audio` element is used to embed audio files, such as music, podcasts, or sound effects, directly into a webpage. 

To make an audio player functional, you typically include the `src` attribute to specify the location of the audio file, and the `controls` attribute so users can interact with the player.

Below is an example of an HTML page that sets up a music player with multiple tracks. Enable the interactive editor to view the page preview. Try removing the `loop` attribute from one of the tracks or changing the text inside the `h2` elements to see how the player changes in the preview window.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Working with the HTML Audio Element</title>
</head>
<body>
  <h1>freeCodeCamp Tunes</h1>

  <h2>Can't Stay Down</h2>
  <p>Artist: Quincy Larson</p>
  
  <audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/can't-stay-down.mp3" loop controls></audio>

  <h2>Cruising for a Musing</h2>
  <p>Artist: Quincy Larson</p>

  <audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/cruising-for-a-musing.mp3" loop controls></audio>

  <h2>Scratching the Surface</h2>
  <p>Artist: Quincy Larson</p>
  <audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/scratching-the-surface.mp3" loop controls></audio>

</body>
</html>
```

Let's break down some of the key features of the `audio` element:

First, there is the `src` attribute:
```html
<audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/can't-stay-down.mp3"></audio>
```
The `src` attribute specifies the URL or file path of the audio resource you want to embed.

Next, there is the `controls` attribute:
```html
<audio src="music-file.mp3" controls></audio>
```
By default, the `audio` element does not have a user interface and will be completely hidden. Adding the `controls` attribute displays the browser's default audio player interface, which includes play/pause buttons, track progress, volume, and mute controls.

Finally, there is the `loop` attribute:
```html
<audio src="music-file.mp3" loop controls></audio>
```
The `loop` attribute is a boolean attribute. When present, it tells the browser to automatically restart the audio track from the beginning once it finishes playing, creating a continuous loop.

### Supporting Multiple Audio Formats
To ensure your audio plays across all modern web browsers, it is sometimes better to nest `<source>` elements inside your `<audio>` element instead of using the `src` attribute directly. The browser will automatically play the first format it supports:

```html
<audio controls>
  <source src="track.ogg" type="audio/ogg">
  <source src="track.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
```
The text inside the opening and closing `<audio>` tags acts as a fallback. If a user is browsing with an older browser that doesn't support HTML5 audio elements, they will see that text instead of the player.

Using the HTML5 `audio` element correctly makes it incredibly simple to integrate sound into your web projects without relying on external plugins.