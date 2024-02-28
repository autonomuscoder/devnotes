1. <b>forEach</b>: Calls a function for each item in an array. Can't be used on empty list
#### Example:
<code>
[1, 2, 3].forEach(function (item, index) {<br>
console.log(item, index);<br>
} )
</code>

So one can do something for each item in an array.

2. <b>Map</b>: Same as forEach but replaces the old items with new items.

#### Example:
<code>
const three = [1, 2, 3];<br>
const doubled = three.map(function (item) {<br>
return item*2;<br>
});
</code>

Doubles the value of each item i.e. the array becomes [2, 4, 6].

3. <b>filter</b>: Iterates over an array and checks each item against a codition for true or false. Generates a new array with the items that yield true.
#### Example:
<code>
const ints = [1, 2, 3];<br>
const evens = ints.filter(function (item) {<br>
return item % 2 ===0;<br>
})
</code>

This checks if each item in the 'ints' array is divisible by two. In other words if they are even or odd. The 'ints' array remains the same. And new array 'evens' is created with truthy items in this case 2

4. <b>Reduce</b>: Iterates over the array and adds the items together to create a new variable with the value of the sum of all the array items.

#### Example: 
<code>
const sum = [1, 2, 3].reduce(function (result, item) { <br>
return result + item;<br>
}, 0 )
</code>

The 0 at the end ensures that the accumulator which is the 'result' parameter in our case initializes with a value of 0

<b>Confusion</b>: Doesn't the accumulator add the items anyway. Why do we need to add the 'item' to it?

<b> Solution</b>: Think of the accumulator as a container that holds the intermediate results. Initially, it's empty (or 0 in our case). As you iterate through the array, you add the relevant data <i>(item)</i> to the container, building up the final result with each addition.
Adding the 'item' also ensures -

- The data type remains consistent
- The summation occurs incrementally

5. <b>Some</b>: This checks if any item in the array meet a certain condition. Even if only one item meets the condition it will return true, otherwise it will return false.

#### Example:

<code>
const hasNegativeNumbers = [1, 2, 3, -1, 4].some(function (item) { <br>
return item < 0; <br>
});
</code>

Checks the array if it has any negative numbers or not. In our case the array has only one negative number so the result is true.


6. <b>Every</b>: Same as some but every time has to meet the condition

#### Example: 
<code>
const allPositiveNumbers = [1, 2, 3].every(function (item) { <br>
return item > 0;<br>
})
</code>

7. <b>Find</b>: Checks every item of the array against a condition, if true returns only the truthy items. Basically one can find specific things in the array hence the name find.

#### Example
<code>
const objects = [{ id: 'a' }, { id: 'b' }, { id: 'c' },];<br>
const found = objects.find(function (item) {<br>
return item.id === 'b';<br>
})
</code>

Searches for the string 'b' and returns only the item or undefined if nothing is found

<b>Find Index</b>: Exactly like find but instead of returning the item itself when true will only return the index of that item.

#### Example:
<code>
const objects2 = [{ id: 'a' }, { id: 'b' }, { id: 'c' },];<br>
const foundIndex = objects2.findIndex(function (item) { <br>
return item.id === 'b';
})
</code>

Searches for 'b', when found returns its index which is 1 in our case.