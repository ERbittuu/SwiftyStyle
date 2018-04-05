# SwiftyStyle 
## "Think Once Twice Thrice... Code Once!" 

```swift
_ = `self` // Learning swift style guide.
```


### Naming Conventions **3 Rules**
* [PascalCase naming conventions](#pascal-case)
* [CamelCase naming conventions](#camel-case)  
* [Constant naming conventions](#constant-naming) 

*** 
***

## Pascal Case
[`class`](#class), [`protocol`](#protocol), [`struct`](#struct), and [`enum`](#enumeration) names should follow *PascalCase naming conventions*.
##### Several words are joined together, and the first letter of every word is capitalized.

#### Class 

*Preferred*

```swift
class OneClass {
	// do something interesting for this class
}

class SubClass : SuperClass {
	// do something interesting for this class
}
```

*Not Preferred*

```swift
class invalidClassName {
	// do something interesting for this class
}

class inval1dCla$$Name : SuperClass {
	// do something interesting for this class
}
```

#### Enumeration

*Preferred*

```swift
enum OneEnumeration {
	// do something interesting for this enumeration
}
```

*Not Preferred*

```swift
enum oTHEr_Enumeration {
	// do something interesting for this enumeration
}

enum nextEnumeratioN {
	// do something interesting for this enumeration
}

enum One-Enumeration {
	// do something interesting for this enumeration
}
```

#### Struct 

*Preferred*

```swift
struct OneStructure {
    // do something interesting for this structure
}
```

*Not Preferred*

```swift
struct One-Structure {
    // do something interesting for this structure
}
```

#### Protocol  

*Preferred*

```swift
protocol OneProtocol {
    // do something interesting for this protocol
}
```

*Not Preferred*

```swift
protocol oneProtocol {
    // do something interesting for this protocol
}
```

*** 
***

## Camel Case
[`methods`](#method-and-selector), [`variables`](#variable), and [`enum values`](#enumeration) names should follow *CamelCase naming conventions* 
##### First letter of the entire word is lowercase, but subsequent first letters are uppercase.

#### Method and selector

*Preferred*
```swift
func oneMethod() {
    // show your hard work in definition
}
```

*Not Preferred*

```swift
func one-method() {
    // show your hard work in definition
}

func SecondMethod() {
    // show your hard work in definition
}

func Method() {
    // show your hard work in definition
}
```

#### Variable 

*Preferred*

```swift
var lastName = "Utsav"
```

*Not Preferred*

```swift
var last_name = "wrong"

var lastname = "also wrong"

var LastName = "another wrong"
```

#### Enumeration 

*Preferred*

```swift
enum Direction {
	case north
	case south
	case east
	case west
}
```

*Not Preferred*

```swift
enum Direction {
	case N0rth
	case Sou-th
	case East
	case WEST
}

// Not Preferred in last swift version 
enum Direction {
	case North
	case South
	case East
	case West
}
```

*** 
***

## Constant Naming

[`Global Constants`](#global-constants-and-local-constants) should follow either *PascalCase naming conventions* or *CamelCase naming conventions*. 
[`Local constants`](#global-constants-and-local-constants) should follow either *PascalCase naming conventions* or *CamelCase naming conventions*. 

#### Global Constants and Local constants

*Preferred*

```swift
let MaxHeight = 42
let maxHeight = 42
let defaultValue = 100
```

*Not Preferred*

```swift
let max_height = 42
let kMaxHeight = 42
let MAXHEIGHT = 42
let DEFAULTVALUE = 1000
```

# Contributing to SwiftyStyle

SwiftyStyle welcomes contributions to our [open source projects on Github](https://github.com/ERbittuu/SwiftyStyle).

Issues
------

Feel free to submit issues and enhancement requests.

Contributing
------------

Please refer to each project's style guidelines and guidelines for submitting patches and additions. In general, we follow the "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull request** so that I can review your changes

NOTE: Be sure to merge the latest from "upstream" before making a pull request!

# Thanks 🍺
