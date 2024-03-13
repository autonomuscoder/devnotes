- <b>Event Bubbling</b>: When an event is bubbled up, it is sent to the parent element first, and then to the parent's parent, and so on. Meaning it can chain on and on from children to parent element which is mostly undesirable.

#### This can be avoided by using stopPropagation() method.

#### example 
<code>
  --- Html ---
  <div class="parent"> <br>
    I am parent <br>
    <div class="child"> <br>
      I am child <br>
    </div> <br>
  </div> <br>
  ---JS <br>
  document.querySelector('button').addEventListener('click', function(e){ <br>
  e.stopPropagation(); <br>
  })
</code>

This stops the event bubbling. So only the child element will receive the event and not the parent.
