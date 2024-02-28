- inside the source folder create new '.tsx' files for new components
- '.tsx' is the extension for typescript or '.jsx' for vanilla js.
- use '.tsx' for react components and '.ts' for normal typescript/config files.
- React components can be made with js functions or classes.
- For modern projects function based components are recommended.
- react namescheme follows PascalCasing
- Writing html inside react code or more precisely js/ts code is called jsx (Javascript XML)
- In jsx you can write any javascript inside curly braces which gives you the power to use dynamic content. For Example,
<code>
function App() {<br>
const name = "Abir";<br>
return (<br>
<div><br>
<h1>Hello! {name}</h1><br>
</div>
)
}
</code>

- Cannot use <b>Class</b> inside the jsx since it is reserved keyword for JS. Instead Use <b>ClassName</b>
- 