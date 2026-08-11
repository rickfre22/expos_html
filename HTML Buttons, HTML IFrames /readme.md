# HTML Buttons
Buttons let users interact with a web page. They can submit forms, run JavaScript, or trigger different actions when clicked.

HTML Button
The HTML <button> element defines a clickable button.

By itself, the button does nothing until you add an action to it.

Example
<button>Click Me</button>
Styling HTML Buttons
Buttons are often styled with CSS:

Example
<button class="mytestbtn">Green Button</button>
Disabled Buttons
Use the disabled attribute to make a button unclickable:

Example
<button disabled>Disabled Button</button>
Tip: Disabled buttons cannot be clicked and usually appear faded.

REMOVE ADS

Button with JavaScript
You can run JavaScript when the user clicks a button using the onclick attribute:

Example
<button onclick="alert('Hello!')">Click Me</button>
Note: You will learn more about JavaScript in our HTML JavaScript chapter.

Button Types
The type attribute defines what a button does when clicked. There are three button types:

type="button" - A normal clickable button (does nothing by default)
type="submit" - Submits a form
type="reset" - Resets all form fields
<button type="button">Normal Button</button>
<button type="submit">Submit</button>
<button type="reset">Reset</button>
Buttons are often used inside forms, which you will learn more about in a later chapter.

For now, just know that a submit button sends the form data to the server, while a reset button clears the form:

Example
<form action="/action_page.php">
  First name: <input type="text" name="fname">
  <button type="submit">Submit</button>
  <button type="reset">Reset Form</button>
</form>
HTML Iframes
An HTML iframe is used to display a web page within a web page.


HTML Iframe Syntax
The HTML <iframe> tag specifies an inline frame.

An inline frame is used to embed another document within the current HTML document.

Syntax
<iframe src="url" title="description"></iframe>
Tip: It is a good practice to always include a title attribute for the <iframe>. This is used by screen readers to read out what the content of the iframe is.

Iframe - Set Height and Width
Use the height and width attributes to specify the size of the iframe.

The height and width are specified in pixels by default:

Example
<iframe src="demo_iframe.htm" height="200" width="300" title="Iframe Example"></iframe>
Or you can add the style attribute and use the CSS height and width properties:

Example
<iframe src="demo_iframe.htm" style="height:200px;width:300px;" title="Iframe Example"></iframe>
REMOVE ADS

Iframe - Remove the Border
By default, an iframe has a border around it.

To remove the border, add the style attribute and use the CSS border property:

Example
<iframe src="demo_iframe.htm" style="border:none;" title="Iframe Example"></iframe>
With CSS, you can also change the size, style and color of the iframe's border:

Example
<iframe src="demo_iframe.htm" style="border:2px solid red;" title="Iframe Example"></iframe>
Iframe - Target for a Link
An iframe can be used as the target frame for a link.

The target attribute of the link must refer to the name attribute of the iframe:

Example
<iframe src="demo_iframe.htm" name="iframe_a" title="Iframe Example"></iframe>

<p><a href="https://www.w3schools.com" target="iframe_a">W3Schools.com</a></p>
REMOVE ADS

Chapter Summary
The HTML <iframe> tag specifies an inline frame
The src attribute defines the URL of the page to embed
Always include a title attribute (for screen readers)
The height and width attributes specify the size of the iframe
Use border:none; to remove the border around the iframe
HTML iframe Tag
Tag	Description
<iframe>	Defines an inline frame
For a complete list of all available HTML tags, visit our HTML Tag Reference.