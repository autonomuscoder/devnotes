== Used to retrieve the text written inside html tags. ==
##### Example:
<code>
const info = document.querySelector(".info");<br>
info.innerText = "hello world";<br>
</code>

Selects the text content of the elements having <i>.info</i> class and changes the text to <i>hello world</i>.

<b>Note</b>: The important thing to note is that while <i>innerText</i> and <i>textElement</i> do the same thing they have some key differences.

- <i>innerText</i> only retrieves visible text while <i>textContent</i> can retrieve both visible and hidden text (invisible due to css or invisible parent elements).
- <i>innerText</i> preserves the formatting and styling of the text but <i>textContent</i> does not.
- So <i>innerText</i> is better where you need to work with the text as it is displayed on the screen styling and all. 
- Whereas <i>textContent</i> is better when you need to access the entire text of an element regardless of its visibility.

In summary:-
![[innertext_vs_textcontent 1.png]]