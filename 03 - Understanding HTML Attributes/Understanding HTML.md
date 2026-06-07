HTML represents the content and structure of a webpage through the use of elements. Most elements will have an opening tag and a closing tag. Sometimes those tags are referred to as start and end tags. In between those two tags, you will have the content. This content can be text or other HTML elements.

Here is another example of a paragraph element. Change the text in the editor to say I love coding! and see the results in the preview window.

```html
<p>I am a paragraph element.</p>
<p>I love coding!</p>
```

Both opening and closing tags start with a left angle bracket (<), and end with a right angle bracket (>), with the tag name placed between these angle brackets. While HTML tag names are case-insensitive, it is a widely accepted convention and best practice to write them in lowercase.

```html
<p>
</p>
```

Here is an example of an image element which is a void element:

```html
<img>
```

Notice that this image element does not have the closing tag and it does not have any content. Void elements cannot have any content and only have a start tag.

Sometimes you will see void elements that use a `/` before the `>` like this:

```html
<img />
```

While many code formatters like Prettier, will choose to include the `/` in void elements, the HTML spec states that the presence of the `/` "does not mark the start tag as self-closing but instead is unnecessary and has no effect of any kind".

In real world development, you will see both forms so it is important to be familiar with both.

If you wanted to display an image, you will need to include a couple of attributes inside your image element. An attribute is a special value used to adjust the behavior for an HTML element.

Here is an example of an image element with a src attribute. Update the value of the src attribute to `"https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg"` and you will see the image change to two cats peacefully sleeping.

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg" />
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" />
```

The src attribute is used to specify the location for that image. For image elements, it's good practice to include another attribute called the alt attribute. The alt attribute is used to provide short, descriptive text for the images.

Here's an example of an image element with the src and alt attributes. Try breaking the image by updating the src value to `"https://.freecodecamp.org/curriculum/cat-photo-app/cats.jpg"`. You will see the image disappear and only the alt text show.

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="Two tabby kittens sleeping together on a couch." />

<img src="https://.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="Two tabby kittens sleeping together on a couch." />
```

So, you might be wondering if HTML by itself is enough to build a website. Well, the answer is: it depends. If you're building a small practice project that only displays text and images, HTML alone might be sufficient. However, if you're creating a modern professional website, you will need to have HTML, CSS, and JavaScript.

HTML is for the content and structure. CSS is for styling. JavaScript is for adding interactivity to your web pages. A good analogy for this is to compare HTML, CSS, and JavaScript with a complete building.

HTML represents the blocks, concrete, and irons that make up the walls. It's the foundation that makes the building strong. CSS represents the interior and exterior design that makes the house look beautiful. JavaScript represents the electrical and water system that ensures uninterrupted access to water and electricity.

An attribute is a value placed inside the opening tag of an HTML element. Attributes provide additional information about the element or specify how the element should behave. Here is the basic syntax for an attribute:

```html
<element attribute="value"></element>
```

The attribute name is followed by an equal sign (=) and a value in quotes. The value can be a string or a number, depending on the attribute.

This first example uses the href and target attributes. The href attribute specifies the URL of a link and the target attribute specifies where to open the link.

Note: The a element, also known as the anchor element, is used to create hyperlinks. The text between the opening and closing a tags is the clickable part users select to navigate.

Enable the interactive editor and change the `href="https://www.freecodecamp.org/news/"` to `href="https://www.freecodecamp.org"`. Now when you click on the link in the interactive editor, you will see the freeCodeCamp homepage in a new browser tab.

Without the href attribute, the link would not work because there would be no destination URL. So you must include this href attribute to make the link functional. The `target="_blank"` enables the link to open in a new browser tab. You will learn more about the target attribute in future lessons.

Other common attributes are the src, and alt, or alternative, attribute - which is used to specify the source of an image and provide alternative descriptive text for the image, respectively.

Enable the interactive editor and change the `src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg"` to `src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg"`. Then change the `alt="Two tabby kittens sleeping together on a couch."` to `alt="Two cats running in the dirt."`.

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="Two tabby kittens sleeping together on a couch."/>

<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/running-cats.jpg" alt="Two cats running in the dirt."/>
```

Similar to the href attribute, the src attribute is required because it specifies the image file to be displayed. The alt attribute is not required, but it is recommended for accessibility purposes. Accessibility means making sure that everyone, including those with disabilities, can use and understand things like websites, apps, and physical spaces. You will learn more about accessibility in the upcoming lessons.

Some attributes are a little unique with their syntax like the checked attribute.

Enable the interactive editor and try clicking on the checkbox in the preview window to see it alternate between a checked and unchecked state.

```html
<input type="checkbox" checked />
```

In the following example, we have an input element with the type attribute set to checkbox. Inputs are used to collect data from users, and the type attribute specifies the type of input. In this case, this input is a checkbox. You will learn more about how inputs work in the upcoming lessons.

The checked attribute is used to specify that the checkbox should be checked by default. The checked attribute does not require a value. If it is present, the checkbox will be checked by default. If the attribute is not present, the checkbox will be unchecked. This is known as a boolean attribute. You will learn more about booleans in general when you get to the JavaScript section.

Enable the interactive editor and try removing the checked attribute from the input. You will see that the checkbox is no longer checked by default.

There are several common boolean attributes you will encounter in HTML, such as disabled, readonly, and required. These attributes are used to specify the state of an element, such as whether it is disabled, read-only, or required.

Here is an example of a text input element that is disabled by default. Enable the interactive editor and try clicking on the input element in the preview window. Now remove the disabled attribute from the input element and you will see that the input is no longer disabled by default. You should now be able to click on it and type inside the field.

```html
<input type="text" disabled>

<input type="text">
```

HTML has many attributes that can be used to customize the behavior and appearance of elements on a webpage. Understanding how to use attributes is essential for creating interactive and accessible web content. Over the next few lessons, you will learn about more HTML attributes and how to use them effectively in your web development projects.
