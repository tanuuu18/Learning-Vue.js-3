# Conditional Rendering


## For conditional rendering, we have 4 directives
<ol>
  <li><b>v-if</b> : This directive accepts a javascript expression that evaluates to wither true or false and will render only is the javascript expression evaluates to a truthy value.</li>

<li><b>v-else</b> : it's always next after the v-if directive, otherwise it will not work.</li>
<li><b>v-else-if</b>: just like else-if ladder</li>
<li><b>v-show</b> :
  <ul>
    <li>  It hide or show the element based on the expression assign to it.</li>
    <li>  It's doing the same thing as v-if.</li>
    <li>The only difference is that v-if will mount the element onto the DOM if the condition evaluates to true and remove the element from the DOM if the condition evaluates to false.</li>
    <li>An element with v-show directive however will always be renderd and remain in the DOM, only the display css property is toggled to show or hide the element.</li>
    <li>
      So, if you have an element that is going to be toggled back and forth in the UI, using <i>v-show</i> is the right approach because, mounting and un-mounting elements onto the DOM can be expensive.
    </li>
    <li>Simply, toggling the css property is more efficient approach which you can do so with <i>v-show</i> directive.</li>
    <li>On the other-hand, if the rendering condition for an elemnt is unlikely to change during runtime or if there are several elements that depend on a single condition <i>v-if</i> is the better choice of directives.</li>
  </ul>
  
  



</li>
  

</ol>

