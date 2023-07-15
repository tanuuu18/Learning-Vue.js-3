# Single File Components


## .Vue file
<ul>
  <li> A *.vue file is a custom file format that uses HTML-like syntax to describe a portion of the UI.</li>
  <li> Each *.vue file consists of three types of top-level language blocks
  <ol>
    <li> < template>< /template> </li>
    <li><script></script></li>
    <li><style></style></li>
  </ol>
    <ul>
      <li>The template block is like the HTML of your UI.</li>
      <li>The script block is where the logic and functionality of your app can be maintained.</li>
      <li>The CSS block is where you specify the styles related to the mark up in the template block.
    </ul>
  </li>
  
</ul>


## Components
<ul>
  <li>A .vue file is called a single file component (SFC)</li>
  <li>As a beginner, there is a lot to learn without having to worry about the component architecture.</li>
</ul>

##
The template block is responsible for the markup and the script block is responsible for the logic of the UI.

Working with .Vue files is wiring up the logic to the markup.

That is, connecting data present in the script block to thr HTML present in the template block.

Declarative programming approach.

Let Vue know how you want to bind your data to the HTML and Vue will take care of the rest.
