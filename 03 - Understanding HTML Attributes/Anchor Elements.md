The a element, also known as the anchor element, is used to create hyperlinks. Hyperlinks allow users to navigate from one page to another, or to a specific location on the same page.

To make an anchor element functional, you must include the href attribute. The href (hypertext reference) attribute specifies the destination URL (web address) that the link points to.

Here is a basic example of an anchor element:

<a href="https://www.freecodecamp.org">Visit freeCodeCamp</a>

The text between the opening and closing a tags ("Visit freeCodeCamp") is the clickable part that the user selects to navigate.

Below is an example of a Travel Agency page using anchor elements. Enable the interactive editor to view the page preview. Try updating the href values of the links or changing the target attributes to see how they behave in the preview window.

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Travel Agency</title>
    <meta
      name="description"
      content="Best Travel Agency World Wide"
    />
  </head>
  <body>
  <h1>Barcelona</h1>
  <p>Barcelona is a great holiday spot. It has sun, sea, and more.</p>
  <h2>Packages</h2>
  <p>We offer an extensive range of holiday solutions to accommodate the needs of all our clients. From daily excursions in the most beautiful cities, to thorough tours of hidden villages and medieval towns to discover Barcelona's lesser-known sides.</p>
<ul>
  <li>
    <a href="https://www.freecodecamp.org/learn">Group Travels</a>
  </li>
  <li>
    <a href="https://www.freecodecamp.org/learn">Private Tours</a>
  </li>
</ul>
<h2>Top Itineraries</h2>
<figure>
  <a href="https://www.freecodecamp.org/learn" target="_blank">
    <img src="https://cdn.freecodecamp.org/curriculum/labs/colosseo.jpg" alt="Colosseum in Rome">
  </a>
  <figcaption>Rome</figcaption>
</figure>

<figure>
  <a href="https://www.freecodecamp.org/learn" target="_blank">
    <img src="https://cdn.freecodecamp.org/curriculum/labs/alps.jpg" alt="The Alps">
  </a>
  <figcaption>Alps</figcaption>
</figure>

<figure>
  <a href="https://www.freecodecamp.org/learn" target="_blank">
    <img src="https://cdn.freecodecamp.org/curriculum/labs/sea.jpg" alt="Beautiful Sea">
  </a>
  <figcaption>Sea</figcaption>
</figure>


Let's break down some of the key features of the anchor element:

First, there is the href attribute, which is required because it specifies the destination of the link. Without the href attribute, the link would not be functional.

Next, there is the target attribute:

<a href="https://www.freecodecamp.org" target="_blank">Visit freeCodeCamp</a>

The target attribute specifies where to open the linked document. Setting target to "_blank" tells the browser to open the link in a new tab or window instead of the current one.

Finally, you can also turn images into links. To do this, you simply wrap an img element inside of an anchor element. In the example above, each travel destination image is nested inside an anchor element. This makes the entire image a clickable link:

<a href="https://www.freecodecamp.org/learn" target="_blank">
  <img src="https://cdn.freecodecamp.org/curriculum/labs/colosseo.jpg" alt="Colosseum in Rome">
</a>

Using anchor elements correctly is essential for building intuitive navigation and connecting your webpages to the rest of the web.


