# Vue.js tips

## How to decide between using v-if or v-show

  v-show will always render, regardless of the truthy-ness of the 
  expression.
  Whereas v-if will only render the content if the expression is true.

Each time the expression toggles, v-show will toggle the CSS display property
of the element while v-if completely destroys/reconstructs the element.

v-if has a quicker initial render but higher toggle costs.
v-show has a slower initial render but lower toggle costs.

Pick v-show if you expect the element to be toggled frequently.
Pick v-if if the element is unlikely to be toggled much at runtime.