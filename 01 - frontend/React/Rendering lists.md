### Code
<code>
function ListGroup() {<br>
  const cities = ["New York", "Paris", "London", "Berlin"];<br>
  return (<br>
    <>
      <h1>List Group</h1>
      <ul className="list-group">
        {cities.map((city) => <li key={city} className="list-group-item">{city}</li>)}
      </ul>
    </>
  )
}


export default ListGroup;

</code>
