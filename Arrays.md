# Arrays

Store an ordered list of values, each called an 'element'.

Arrays can only sort values of **the same type**, and are indexed starting from 0. The position of the elements are the same unless you come in and change it.

### Most Useful Case:
When you want things to maintain their order, or if you want to sort them. 

	let highScores = [100, 98, 56, 54, 32, 0]
	var countries = ["Canada", "Brazil", "Mexico"]

If you don't know what you want your array to be just yet, you can declare a **constant** without setting a **value**. You can only do this with a variable if you will want to add to it.


	var countries: [String] = []
	countries.append("Uruguay")
	// you've just added a country to an empty array!

## Subscripting
 
Easy peasy stuff, this is the way to reference a SPECIFIC element in an array.

	countries[0] // returns "Canada"
	countries[1] // returns "Brazil"


## Accessing Ranges

The best way to access a small range of elements in an array is by specifying a range inside the brackets to represent the indexes you want.

	let firstFewCountries = countries[1..3] // would return ["Brazil", "Mexico", "Uruguay"]
	
That makes a small segment called an Array Slice, NOT an array, so you'll have to cast it as an array to index it.

	let firstFewCountries = Array(countries[1..3])


# Methods

## .append
We know that this one adds an element of the same type.

## .removeAll()
This empties the array. 

## .isEmpty()
This returns a boolean **false** if the array has elements and **true** if the array lacks them.

## .count 
Returns an Int equal to the number of elements in the array.

## .first
Returns the first element in the array...is optional surprisingly, but that's because there's a possibility the array is empty.

A good way to unwrap the optional if it exists is:

	if let first = countries.first {
		print(first)
	}


## .contains()
See if an array contains a certain value, returns a boolean.

## .remove(at: )/.removeLast()
You get what this does.

## Add a fixed number of Elements

	
	let model = ThoughtModel()
	let thoughts = [ThoughtModel](repeating: model, count: 25)

## Get the first/last from an array satisfying a condition

	let loudestSong = songs.first(where: { $0.songVolume > 80 })
	print(loudestSong?.title)
	// this is an optional because first element might not exist (remember from before?)

	let quietestSong = songs.last(where: { $0.songVolume < 20 })
	
	// Longhand
	let firstSong = songs.first { song in
		return song.id > 50
	}




