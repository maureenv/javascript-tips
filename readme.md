# Javascript Tips
### set()
Remove duplicates


    const dups = [ 'cat', 'dog', 'pig', 'cat']
	const removed = [ ...new Set(dups)]

### Loops
- **map** - for creating new array
- **for each** - no new array needed
- **for (const element of array)** - fastest

### Call function with default values

    const calculateTotal = ( item, { shipping = 10, discount = 0 } = {}) => {}
    calculateTotal( item, { shipping: 0 })

### JS Reference VS Value
- in JS anything that isn't a primitive value like string, number or boolean, such as array and object is passed by reference **NOT** value

    let c = [1,2] // c === d & c == d both true since d is refernecing c in memory.
    let d = c

    let c = [1,2] // c === d & c == d are both false since an array/object is checking the memory address and they're both set to different memory addresses.
    let d = [1,2]
