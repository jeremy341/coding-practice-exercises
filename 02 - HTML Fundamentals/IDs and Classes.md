The id attribute adds a unique identifier to an HTML element.

Here is an example of an h1 element with an id of title.

Below the h1 element, add an h2 element with an id set to "subtitle". You can write whatever text you like for the h2 and you will see the changes in the preview window. To interact with the example, you will need to enable the interactive editor.

<h1 id="title">Movie Review Page</h1>
<h2 id="subtitle">A personal take on the greatest movie of all time.</h2>

You can reference the id name of title within your JavaScript or CSS. Here's a CSS example referencing the id of title to change the text color to red.

NOTE: Some CSS has been provided for you in this interactive example. Don't worry about trying to understand the CSS code because you will learn more about that in future lessons. But if you want to see the text color change to blue, enable the interactive editor, click on the styles.css tab and change the color: red; to color: blue;.

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta
       name="viewport"
       content="width=device-width, initial-scale=1.0" />
    <title>Review page Example</title>
    <link rel="stylesheet" href="./styles.css" />
  </head>
  <body>
    <h1 id="title">Movie Review Page</h1>
  </body>
</html>

#title {
  color: red;
}

The hash symbol (#) in front of title, tells the computer you want to target an id with that value. id names should not be used more than once, and they should always be unique. Another thing to note about id values, is that they cannot have spaces in them. Here is an example of applying the words main and heading to an id attribute value:

<h1 id="main heading">Main heading</h1>

Browsers will see this space as part of the id, which will lead to unwanted issues when it comes to styling and scripting. ID attribute values should only contain letters, digits, underscores, and dashes.

In contrast to the id attribute, the class attribute value does not need to be unique and can contain spaces.

Here is an example of applying a class called box to a div element:

<div class="box"></div> 

If you want to add multiple classes to an element, you can do so by separating the names with a space. Here is an updated example applying multiple classes to multiple div elements.

<div class="box red-box"></div>

Here is another example of applying multiple classes to multiple div elements.


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta
       name="viewport"
       content="width=device-width, initial-scale=1.0" />
    <title>Colored boxes example</title>
    <link rel="stylesheet" href="./styles.css" />
  </head>
  <body>
    <div class="box red-box"></div>
    <div class="box blue-box"></div>
    <div class="box red-box"></div>
    <div class="box blue-box"></div>
  </body>
</html>

.box {
  width: 100px;
  height: 100px;
}

.red-box {
  background-color: red;
}

.blue-box {
  background-color: blue;
}

So, to recap, when should you use an id versus a class? Classes are best used when you want to apply a set of styles to many elements. If you want to target a specific element, it is best to use id because those values need to be unique.