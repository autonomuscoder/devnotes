Can be used to get the text content of an element and all its child components. Useful to manipulate text written inside html tags and elements using javascript. Can not change the html tags themeselves though. <b>Example</b>

#### Reading textcontent
<code>
const paragraph = document.getElementById('myParagraph');<br>
const content = paragraph.textContent; // Retrieves the paragraph's text

</code>

#### Emptying text content
<code>
const listItem = document.querySelector('li');<br>
listItem.textContent = ''; // Empties the list item's content
</code>

#### Replacing text content
<code>
const header = document.getElementsByTagName('h1')[0];<br>
header.textContent = 'Welcome to my website!'; // Replaces the header's content
</code>