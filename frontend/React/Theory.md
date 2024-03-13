### How react works

- When a react code is written and executed in the browser the browser create a virtual lightweight DOM (almost like the js DOM but lighter and in memory) which represents all the components in that react code.
- Now when the state or data of the code is updated than react creates a updated version of the DOM. It then compares the DOMs and only updated the parts or nodes of the DOM that have changed.
- This updating of the node is done using the 'ReactDOM' library. (which should always come with the create reach app or the like as it is a builtin component of react).
- 