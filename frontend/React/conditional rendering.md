- Most popular way is to use the ternary operator
<code>
{items.length === 0 ? \p\no item found \p\: null}
</code>

- Most of the time one can also use and operators (&&) for the use of logic


<b>Note</b>: a true condition and a value if compared with an and operator will always render the value.

<code>
{items.length===0 && \p\no item found\p\}
</code>
Will always render the p element if true. This is widely used for conditional rendering in react