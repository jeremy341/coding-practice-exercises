An HTML entity, or character reference, is a set of characters used to represent a reserved character in HTML.

Let's say you wanted to display the text "This is an <img/> element" on the screen. If you use the code currently in the editor, it won't display the desired result. Even if you added src and alt attributes to the example, it would show an image in the middle of the paragraph. Not the desired result. To interact with the example, you will need to enable the interactive editor.

<p>This is an <img /> element.</p>

When the HTML parser sees the less than (<) symbol followed by an HTML tag name, it interprets that as an HTML element. That is why you are not getting the desired result of "This is an <img /> element" on the screen.

Enable the interactive editor and try adding a &lt;p&gt;learning is fun&lt;/p&gt; below the paragraph element. You should see <p>learning is fun</p> on the screen.

<p>This is an &lt;img /&gt; element</p>
&lt;p&gt;learning is fun&lt;/p&gt;

These types of character references are known as named character references. Named references start with an ampersand sign (&) and end with a semicolon (;). By using a named character reference, the HTML parser will not confuse this with an actual HTML element.

Another type of character reference would be the decimal numeric reference. This character reference starts with an ampersand sign (&) and a hash symbol (#), followed by one or more decimal digits, followed by a semicolon (;).

Here is an example of using a decimal numeric reference for the less than symbol.

Enable the interactive editor and change the code to see different symbols. You can use  &#169; for the copyright symbol and  &#174; for the registered trademark symbol.

&#60;
&#169;
&#174;

The last type of character reference would be the hexadecimal numeric reference. This character reference starts with an ampersand sign (&), a hash symbol (#), and the letters x or X. Then it is followed by one or more ASCII hex digits and ends with a semicolon.

Here is an example of using the hexadecimal numeric reference for the less than symbol. Enable the interactive editor and change the code to see different symbols. You can use  &#x20AC; for the Euro sign and &#x03A9; for the capital Greek letter omega.

&#x3C;
&#x20AC;
&#x03A9;

