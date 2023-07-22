# 16. Methods


# Lists and Keys


## Key attribute
<ul>
  <li>A common practice and also recommended to provide a key attribute with the <b>v-for</b> directive.</li>
  <li>Key is a special attribute which is primarily used as a hint for Vue's virtual DOM algorithm to identify nodes when diffing the new DOM tree with the old DOM tree</li>
  <li>The key attribute helps Vue identify which items in a list have changed, are added or removed and plays a crucial role in handling UI updates correctly and efficiently.</li>
  <hr>
  <li>The key special attribute is primarily used as a hint for Vue's virtual DOM algorithm to identify nodes when diffing the new list of nodes against the old list.</li>
  <li>When used with the <b><i>v-for</i></b> directive, the key attribute should always have a unique value in each iteration.</li>
  <li>Without keys, Vue uses an algorithm that minimizes element movement and tries to patch/reuse elements of the same type in-place as much as possible.</li>
  <li>Not using keys is only suitable when your list render output does not rely on temporary DOM state or child component state.</li>
  <li>Although the default behaviour of patching is more efficient, it can lead to problems.</li>
  <li>A typical value to provide to the key attribute is the <b>id property</b> in an object. But any unique property will do as long as its non non-primitive value like objects or arrays.</li>
</ul>




