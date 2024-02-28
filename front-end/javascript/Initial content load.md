one can listen to initial content loading or DOM loading using the <i>DOMContentLoaded</i> event. Since this is an event eventlisteners can be added to it.
#### Example:
<code>
let currentItem = 0;

// load initial content
window.addEventlistener("DOMContentLoaded", () => {<br>
const item = reviews[currentItem];<br>
img.src = item.img;<br>
author.textContent = item.name;<br>
job.textContent = item.job;<br>
info.textContent = item.text;<br>
})
</code>

One can use something like the above example to load set the first content to load after first load time of the page by leveraging the <i>DOMContentLoaded</i> event