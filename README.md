# SwiftyStyle 
## "Think Once Twice Thrice... Code Once!" 

```swift
_ = `self` // Learning swift style guide.
```


### Naming Conventions **3 Rules**
* [PascalCase naming conventions](#pascal-case)
* [CamelCase naming conventions](#camel-case)  
* [Constant naming conventions](#constant-naming) 

### Whitespace Rule **10 Rules**
* [Arrow Whitespace](#arrow-whitespace) 
* [Angle Bracket Whitespace](#angle-bracket-whitespace) 
* [Colon Whitespace](#colon-whitespace) 
* [Comma Whitespace](#comma-whitespace) 
* [Operator Whitespace (only in operator declarations)](#operator-whitespace) 
* [Leading Whitespace](#leading-whitespace) 
* [Parentheses Whitespace](#parentheses-whitespace) 
* [Trailing Whitespace](#trailing-whitespace) 
* [Comment Whitespace](#comment-whitespace) 
* [Function Whitespace](#function-whitespace) 

### Important **8 Rules**
* [Indentation style](#indentation-style)
* [Redundant Parentheses](#redundant-parentheses)
* [Force Casts](#forced-type-cast)
* [Multiple Imports](#multiple-imports)
* [Terminating Semicolon](#terminating-semicolon)
* [TODO Syntax](#todo-syntax)
* [Redundant Optional Binding](#redundant-optional-binding)
* [Trailing Closure](#trailing-closure)

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

// Not Preferred in latest swift version 
enum Direction {
	case North
	case South
	case East
	case West
}
```

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

## Arrow Whitespace

 Single space prefer @before and @after '->' to ' -> '.
 
Examples:

#### Function and Closure declarations

*Preferred*

```swift
func loginCheck() -> Int {
  return 1 + 2
}

list.map() {
  (name) -> Int in
  return 1
}

class SomeClass: SomeSuperClass {
      // something goes here
}
```

*Not Preferred*

```swift
func loginCheck()->Int {
  return 1 + 2
}

list.map() {
  (name)  ->  Int in
  return 1
}

class SomeClass: SomeSuperClass{
}
```

#### Subscript declarations

*Preferred*

```swift
struct User {
    let multiplier: Int

    subscript(index: Int) -> Int {
        return multiplier * index
    }
    // do something interesting
}
```

*Not Preferred*

```swift
struct User {
    let multiplier: Int

    subscript(index: Int)-> Int {
        return multiplier * index
    }
    // do something interesting
}

struct SomeStruct : SomeParentStruct   {
}
```

#### Function Types

*Preferred*

```swift
func sumOfTwo()) -> (Int, Int) -> (Int) {
  // do something interesting
}
```

*Not Preferred*

```swift
func sumOfTwo() -> (Int, Int)-> (Int) {
  // do something interesting
}

func sumOfTwo() -> (Int, Int)  -> (Int){
  // do something interesting
}
```

*** 

## Angle Bracket Whitespace

There should be no whitespace @before or @after an opening chevron `<` and before the closing chevron `>`.

 Examples:
 
#### Generics

*Preferred*

```swift
func simpleMax<T: Comparable>(x: T, _ y: T) -> T {
    if x < y {
        return y
    }
    return x
}
```

*Not Preferred*

```swift
func simpleMax < T: Comparable >(x: T, _ y: T) -> T {
    if x < y {
        return y
    }
    return x
}
```

#### An Exception : Operator Declarations

In some case required space while using opening angle bracket. The opening angle bracket (if used) in an operator declaration must have a single space preceding it.

Example:  

*Preferred*

```swift
func ++< <T where T: Comparable>(op1: T, op2: T) -> Bool {
}
```

*Not Preferred*

```swift
func ++<<T where T: Comparable>(op1: T, op2: T) -> Bool {
}
```

***

## Colon Whitespace

There should be no whitespace preceding the colon, exactly one whitespace after the colon for:
* [`class`](#class-struct-protocol-and-extension-declarations),  [`var`](#variable-declarations), [`struct`](#class-struct-protocol-and-extension-declarations), [`protocol`](#class-struct-protocol-and-extension-declarations), [`extension`](#class-struct-protocol-and-extension-declarations), [`func`](#function-declarations), and [`tuple`](#tuple-declarations) declarations
* [`dict`](#dictionary-literals-and-types) literals and types
* [`case`](#case-statements) statements

However Exception is for [conditional expressions](#conditional-expressions) there should be a single whitespace @before and @after the colon.
#### Variable declarations

*Preferred*

```swift
var x: Int = 2
```

*Not Preferred*

```swift
var x : Int
var success:   Bool
```
#### Dictionary literals and types

*Preferred*

```swift
var x = [ "index": 1, "index": 2 ]
var y: [ Int: String ]
```

*Not Preferred*

```swift
var x = [ "index" : 1, "index":  2]
var y: [ Int :    String ]
```

#### Case statements

*Preferred*

```swift
switch character {
    case "a": 
        print(a)
    default: 
        alert()
}
```

*Not Preferred*

```swift
switch character {
case "a" : 
    print(a)
default :     
    alert()
}
```

#### Class, Struct, Protocol, and Extension declarations

*Preferred*

```swift
class SubClass: BaseClass {
    // do something interesting
}

struct SubStruct: BaseStruct {
    // do something interesting
}

protocol SubProtocol: BaseProtocol {
    // do something interesting
}

extension BaseClass: BaseProtocol {
    // do something interesting
}
```

*Not Preferred*

```swift
class SubClass : BaseClass {
    // do something interesting
}

struct SubStruct:  BaseStruct {
    // do something interesting
}

protocol SubProtocol:AnotherProtocol {
    // do something interesting
}

extension BaseClass : BaseProtocol {
    // do something interesting
}
```

#### Tuple declarations

*Preferred*

```swift
var someTuple = (top: 10, bottom: 12)  
```

*Not Preferred*

```swift
var someTuple = (top:10, bottom : 12)  
```

#### Function declarations

*Preferred*

```swift
func someFunction<T: SomeClass, U: SomeProtocol>(someT: T, someU: U) {
}
```

*Not Preferred*

```swift
func someFunction<T : SomeClass, U:SomeProtocol>(someT: T, someU: U) {
}
```

#### Conditional expressions

*Preferred*

```swift
var x = condition ? a : b
```

*Not Preferred*

```swift
var x = condition ? a: b
var x = condition ? a   : b
```

***

## Comma Whitespace

Prefer no spaces before and exactly one space after a comma (',' to ', ') in the following structures:

* Generics

*Preferred*

```swift
func someFunction<T: SomeClass, U: SomeProtocol>(someT: T, someU: U) {
    // function body goes here
}

func someFunction<T: SomeClass, U: SomeProtocol,
	V: AnotherClass>(someT: T, someU: U) {
    // function body goes here
}
```

*Not Preferred*

```swift
func someFunction<T: SomeClass,U: SomeProtocol>(someT: T, someU: U) {
    // function body goes here
}

func someFunction<T: SomeClass , U: SomeProtocol>(someT: T, someU: U) {
    // function body goes here
}
```

* Type Inheritance Clauses

*Preferred*

```swift
class Bicycle: Vehicle, TwoWheeler {
    var hasBasket = false
}
```

*Not Preferred*

```swift
class Bicycle: Vehicle,  TwoWheeler {
    var hasBasket = false
}
```

* Condition Clauses

*Preferred*

```swift
if x < 2, 
   var y = val {
   println(x + y)
}

if x < 2, var y = val {
    println(x + y)
}

if let roomCount = john.residence?.numberOfRooms, 
   roomCountTwo = john.residence?.numberOfRooms {
   println("John's residence has \(roomCount) room(s).")
}
```

*Not Preferred*

```swift
if x < 2 , var y = val {
    println(x + y)
}

if (x < 2), var y = val {
    println(x + y)
}

if let roomCount = john.residence?.numberOfRooms,roomCountTwo = john.residence?.numberOfRooms {
    println("John's residence has \(roomCount) room(s).")
}
```

* Availability Arguments

*Preferred*

```swift
if #available(iOS 9, OSX 10.10, *) {
    // Use iOS 9 APIs on iOS, and use OS X v10.10 APIs on OS X
}
```

*Not Preferred*

```swift
if #available(iOS 9, OSX 10.10,*) {
    // Use iOS 9 APIs on iOS, and use OS X v10.10 APIs on OS X
}
```
* Generic Argument Lists

*Preferred*

```swift
struct Dictionary<Key: Hashable, Value>: CollectionType {}
```

*Not Preferred*

```swift
struct Dictionary<Key: Hashable,   Value>: CollectionType {}
```

* Pattern Initializer Lists

*Preferred*

```swift
let numX = 2, func_y = { x in println(x) }
```

*Not Preferred*

```swift
let numX = 2 , func_y = { x in println(x) }
```

* Parameter Lists

*Preferred*

```swift
func initialize(x: Int, y: Int, z: Int) {}
```

*Not Preferred*

```swift
func initialize(x: Int,y: Int,z: Int) {}
```

* Enum Case Lists

*Preferred*

```swift
enum Planet {
    case Mercury, Venus, Earth, Mars, Jupiter, Saturn, Uranus, Neptune
}

enum Planet : Int {
    case Mercury = 0, Venus, Earth, Mars, Jupiter, Saturn, Uranus, Neptune
}
```

*Not Preferred*

```swift
enum Planet {
    case Mercury,Venus, Earth, Mars,  Jupiter, Saturn, Uranus, Neptune
}

enum Planet {
    case Mercury = 0 ,Venus = 1,Earth = 2, Mars = 4,  Jupiter= 5, Saturn = 6, Uranus= 7, Neptune= 9
}
```

* Tuple Pattern Lists

*Preferred*

```swift
var (x, y): (Int, Int)
```

*Not Preferred*

```swift
var (x,y): (Int , Int)
```

* Array Literal Items

*Preferred*

```swift
shoppingList += ["Chocolate Spread", "Cheese", "Butter"]
```

*Not Preferred*

```swift
shoppingList += ["Chocolate Spread" , "Cheese",  "Butter"]
```

* Dictionary Literal Items

*Preferred*

```swift
var airports: [String: String] = ["YYZ": "Toronto Pearson", "DUB": "Dublin"]
```

*Not Preferred*

```swift
var airports: [String: String] = ["YYZ": "Toronto Pearson","DUB": "Dublin"]
```

* Capture List Items

*Preferred*

```swift
lazy var someClosure: Void -> String = {
    [unowned self, weak delegate = self.delegate!] in
    // closure body goes here
}
```

*Not Preferred*

```swift
lazy var someClosure: Void -> String = {
    [unowned self , weak delegate = self.delegate!] in
    // closure body goes here
}
```

* Paranthesized Expressions

*Preferred*

```swift
var arr = [ (1, 2, 3), (3, 4, 5) ]
```

*Not Preferred*

```swift
var arr = [ (1,2, 3), (3 , 4, 5) ]
```

* Switch Case Item Lists

*Preferred*

```swift
switch character {
    case "a", "e", "i", "o", "u": 
        continue
    default: 
        print(character)
}
```

*Not Preferred*

```swift
switch character {
case "a","e","i","o", "u": 
    continue
default: 
    print(character)
}
```

*** 

## Operator Whitespace

Single space at both side of operator in operator declarations.

*Preferred*

```swift
infix operator -+* { precedence 70 associativity right }
```

*Not Preferred*

```swift
infix operator-+* { precedence 70 associativity right }

infix operator -+*  { precedence 70 associativity right }

infix operator -+*{ precedence 70 associativity right }

infix operator  -+* { precedence 70 associativity right }
```

*** 

## Leading Whitespace
Check that source files begin with a non-whitespace character or blank line.

*Preferred*
```swift
1 //
2 //  FileName.swift
3 //  ProjectName
4 //
5 // Copyright information....
6 //
.
. 
.
12 import Foundation
```
```swift
1 import Foundation
2 import UIKit
```

*Not Preferred*

```swift
1 ¬
2 import Foundation
```
```swift
1     import Foundation
```

*** 

## Parentheses Whitespace
There should be no whitespace immediately before/after an opening parenthesis `(` and before the closing parenthesis `)`.

#### Functions

*Preferred*

```swift
func sum(a: Int, b: Int) -> Int {
  return a + b;
}

print("Hello, World!")
```

*Not Preferred*

```swift
func sum ( a: Int, b: Int ) -> Int {
  return a + b;
}

print( "Hello, World!" )
```

#### Tuples

*Preferred*

```swift
let tuple = (5, 2)
```

*Not Preferred*

```swift
let tuple = ( 5, 2 )
```

#### Conditionals

*Preferred*

```swift
if (someCondition) {
  ...
}
```

*Not Preferred*

```swift
if ( someCondition ) {
  ...
}
```

#### Initializers

*Preferred*

```swift
class SomeClass {
  init() {
  }
}
```

*Not Preferred*

```swift
class SomeClass {
  init ( ) {
  }
}
```

*** 

## Trailing Whitespace
remove whitespace after the last non-whitespace character on each line until the newline.

*Preferred*

```swift
let number = 42¬
```

*Not Preferred*

```swift
let number = 42 ¬
print("Hello white space")        ¬
```

*** 

## Comment Whitespace

Prefer *at least one* whitespace character after a comment opening symbol (`//`, `///`, `/*`, or `/**`) and *at least one* whitespace character before a comment closing symbol (`*/`).

*Preferred*

```swift
// This is a comment line 

/// This is a documentation comment line

/* This is a
multi-line comments */

/* This is a
multi-line comments
*/

/** This is a 
documentation multi-line
comments
*/
```

*Not Preferred*

```swift
//This is a comment

///This is a documentation comment

/*This is a
multi-line comment*/

/**This is a multi-line
documentation comment */
```

*** 

## Function Whitespace

Every function and method declaration should have 1 blank line before and after itself. in exception if function is start of a file.

Comments immediately before a function declaration (no blank lines between them and the function) are considered to be part of the declaration.

*Preferred*

```swift
func function1() {
  var text = 1
  var text = 2
}

function1()

// a comment
func function2() {
  // something goes here
}

struct SomeStruct {

  func function3() {
    // something goes here
  }

  func function4() {
    // something else goes here
  };

}

func function5() {
  // something goes here
}
```

*Not Preferred*

```swift
func function1() {
  var text = 1
  var text = 2
}
function1()
// a comment
func function2() {
  // something goes here
}

struct SomeStruct {
  func function3() {
    // something goes here
  }

  func function4() {
    // something else goes here
  };
}
func function5() {
  // something goes here
}
```

## Indentation style
Definitions of
[`init`](#initializers), [`class`](#classes), [`enum`](#enums), [`struct`](#structs), [`function`](#functions), [`protocol`](#protocols), [`extension`](#extensions), [`closure`](#closures), [Getters and Setters](#getters-and-setters) (`set`, `get`), [Control flow constructs](#control-flow-constructs) (`if`, `else if`, `else`, `switch`, `for`, `while`, `repeat-while`) 

Opening curly braces go on the same line as the corresponding statement, separated by a space. and closing brace at the end is on the same indentation level as the header of the function at a line of its own. 

Examples:
#### Initializers

*Preferred*

```swift
init(name: String) {
   self.name = name
}
```

*Not Preferred*

```swift
init(name: String) 
{
   self.name = name
}
```

#### Classes

*Preferred*

```swift
class OneClass {
}

class OneClass: SuperClass {
}
```

*Not Preferred*

```swift
class OneClass
{
}

class OneClass: SuperClass{
}
```

#### Structs

*Preferred*

```swift
struct OneStruct {
}

struct OneStruct : SuperStruct {
}
```

*Not Preferred*

```swift
struct OneStruct
{
}

struct OneStruct : SuperStruct  {
}
```

#### Functions

*Preferred*

```swift
func callMe() {
}

func isOk () -> Bool {
}
```

*Not Preferred*

```swift
func callMe()
{
}

func isOk () -> Bool
{
}
```

#### Control flow constructs

- if, else if, and else statement

*Preferred*

```swift
if i > 2 {

} else if i < 10 {

} else {

}
```

*Not Preferred*

```swift
if i > 2
{

}
else if i < 10
{
}
else
{
}
```

- switch statement

*Preferred*

```swift
switch character {
    case "a", "e", "i", "o", "u": 
        continue
    default: 
        print(character)
}
```

*Not Preferred*

```swift
switch character 
{
    case "a", "e", "i", "o", "u": 
        continue
    default: 
        print(character)
}
```

- for loop

*Preferred*

```swift
for name in names {

}
```

*Not Preferred*

```swift
for name in names 
{

}
```

- while loop

*Preferred*

```swift
while true {

}
```

*Not Preferred*

```swift
while true
{

}
```

- repeat-while loop

*Preferred*

```swift
repeat {

} while true
```

*Not Preferred*

```swift
repeat
{

} while true
```

#### Protocols

*Preferred*

```swift
protocol XProtocol {

}

protocol XProtocol : YProtocol {

}
```

*Not Preferred*

```swift
protocol XProtocol
{

}

protocol XProtocol : YProtocol
{
}

```

#### Enums

*Preferred*

```swift
enum SomeEnum {
    case n, e, w, s
}

enum SomeEnum {
    case n
    case e
    case w
    case s
}

enum SomeEnum: Int {
    case n, e, w = 5, s
}
```

*Not Preferred*

```swift
enum SomeEnum
{
    case n, e, w, s
}

enum SomeEnum
{
    case n
    case e
    case w
    case s
}

enum SomeEnum: Int
{
    case n, e, w = 5, s
}
```

#### Closures

*Preferred*

```swift
func closerFunc () -> () {
// closure
}
```

*Not Preferred*

```swift
func closerFunc () -> ()
{
// closure
}
```

#### Setters and Getters

- set

*Preferred*

```swift
var age : Double {
    set {
        oldValue = newValue / 2
    }
}
```

*Not Preferred*

```swift
var age : Double 
{
    set 
    {
        oldValue = newValue / 2
    }
}
```

- get

*Preferred*

```swift
var age : Double {
    get {
        oldValue = newValue / 2
    }
}
```

*Not Preferred*

```swift
var age : Double 
{
    get 
    {
        oldValue = newValue / 2
    }
}
```

#### Extensions

*Preferred*

```swift
extension newExtension {
}
```

*Not Preferred*

```swift
extension newExtension
{
}
```

***

## [redundant-parentheses]
[Control flow constructs](#control-flow-constructs) (`if`, `else if`, `switch`, `for`, `while`, `repeat-while`, and `guard` statements), [Exception handling constructs](#exception-handling-constructs) (`throw`, and `do/catch` statements), and [Initializers](#initializers) (`array`, `dictionary`, `initializer patterns`) should not be enclosed in parentheses.

Additionally, method calls with no parameters and a trailing closure should not have empty parentheses following the method name.

#### Control flow constructs

- if, else if statement

*Preferred*

```swift
if i < 2 {

} else if 10 > i {
}
```

*Not Preferred*

```swift
if (i < 2) {

} else if (10 > i) {
}
```

- switch statement

*Preferred*

```swift
switch character {
    case "a", "e", "i", "o", "u": 
        continue
    default: 
        print(character)
}
```

*Not Preferred*

```swift
switch (character) {
    case "a", "e", "i", "o", "u": 
        continue
    default: 
        print(character)
}
```

- for loop

*Preferred*

```swift
for name in names {

}
```

*Not Preferred*

```swift
for (name in names) {

}
```

- while loop

*Preferred*

```swift
while true {

}
```

*Not Preferred*

```swift
while (true) {

}
```

- repeat-while loop

*Preferred*

```swift
repeat {

} while true
```

*Not Preferred*

```swift
repeat {

} while (true)
```

- guard clause

*Preferred*

```swift
guard true else {   }
```

*Not Preferred*

```swift
guard (true) else {   }
```

#### Exception handling constructs
- do/catch statement

*Preferred*

```swift
do  {

} catch SomeException {

}
```

*Not Preferred*

```swift
do  {

} catch (SomeException) {

}
```

- throw statement

*Preferred*

```swift
throw SomeException
```

*Not Preferred*

```swift
throw (SomeException)
```

#### Initializers

- array items

*Preferred*

```swift
var list: [String] = ["Hello", "Hi"]
```

*Not Preferred*

```swift
var list: [String] = [("Hello"), ("Hi")]
```

- dictionary items

*Preferred*

```swift
var name: [String: String] = ["first": "Utsav", "last": "Patel"]
```

*Not Preferred*

```swift
var name: [String: String] = [("first"): ("Utsav"), ("last"): ("Patel")]
```

- initializer patterns

*Preferred*

```swift
var x: Int = 2
var y: String = "Hi"
var x = 2
```

*Not Preferred*

```swift
var x: Int = (2)
var y: String = ("Hi")
var x = (2)
```

#### Method calls

*Preferred*

```swift
items.map {
  item in item.transform()
}
```

*Not Preferred*

```swift
items.map() {
  item in item.transform()
}
```

*** 

## Forced Type Cast
Avoid using the forced form of the type cast operator (`as!`) 
 
Use The conditional form of the type cast operator (`as?`) is safer and should be used when possible.

*Preferred*

```swift
if let movie = item as? Movie {
    print("Movie: '\(movie.name)', dir. \(movie.director)")
}
```

*Not Preferred*

```swift
let movie = item as! Movie
print("Movie: '\(movie.name)', dir. \(movie.director)")
```

*** 

## Multiple Imports
Multiple `import` statements should not be defined on a single line.

*Preferred*

```swift
import Foundation
import Cocoa
```

*Not Preferred*

```swift
import Foundation; import Cocoa
```

*** 

## Terminating Semicolon

Swift does not require a semicolon after each statement in your code unless you wish to combine multiple statements on a single line. 

Do not write multiple statements on a single line separated with semicolons if not required.

#### Imports

*Preferred*

```swift
import Foundation
```

*Not Preferred*

```swift
import Foundation;
```


#### Enums and enum cases

*Preferred*

```swift
enum CompassPoint {
	case north
	case south
	case east
	case west
}

enum CompassPoint {
	case north, south, east, west
}
```


*Not Preferred*

```swift
enum CompassPoint {
	case north;
	case south;
	case east;
	case west;
};

enum CompassPoint {
	case north, south, east, west;
};
```

#### Protocols

*Preferred*

```swift
protocol OneProtocol {
	var name: String { get }
	func isProblem() -> Bool
	func callMe(number: PhoneNumber)
}
```

*Not Preferred*

```swift
protocol SomeProtocol {
	var name: String { get };
	func isProblem() -> Bool;
	func callMe(number: PhoneNumber);
};
```

#### Extensions

*Preferred*

```swift
extension NewType {

}
```

*Not Preferred*

```swift
extension NewType {

};
```

#### Structs

*Preferred*

```swift
struct NewStruct {
    var x: String // variables
}
```

*Not Preferred*

```swift
struct NewStruct {
    var x: String // variables
};
```

#### Classes

*Preferred*

```swift
class NewClass {
	let b = 2 // constants
}
```

*Not Preferred*

```swift
class NewClass {
	let b = 2 // constants
};
```

#### Loops

*Preferred*

```swift
// while loop
while true {

}

// for loop
for name in names {
}

// repeat while
repeat {

} while true
```

*Not Preferred*

```swift
// while loop
while true {

};

// for loop
for name in names {
};

// repeat while
repeat {

} while true;
```

***

## Todo Syntax
TODO comments should be defined separately using non-nested single line comments. 

They should adhere to the `<TODO: description>` or `<TODO(developer-name): description>` syntax. Empty TODO comments will be flagged.

*Preferred*

```swift
// TODO: add todo comments
// TODO(dev-name): add todo comments
```

*Not Preferred*

```swift
// TODO:

/// TODO: Documentation comments should not have TODOs

//// TODO: Nested comments should not have TODOs

// //TODO: Nested comments should not have TODOs

// TODO: Nested comments should not have TODOs // some comment

//// TODO: Nested comments should not have TODOs
```

*** 

## Redundant Optional Binding

Optional binding lists should not have consecutive `var`/`let` bindings.  

All constants must be preceded by at most one `let` binding.  

All variables must be preceded by only one `var` binding.

*Preferred*

```swift
if var a = a, b = b, c = c, c != 0 {
    print("(a + b) / c = \((a + b) / c)")     // (a + b) / c = 5
}

if let a = a, b = b, var c = c, c != 0 {
    print("(a + b) / c = \((a + b) / c)")     // (a + b) / c = 5
}
```

*Not Preferred*

```swift
if var a = a, var b = b, var c = c, c != 0 {
    print("(a + b) / c = \((a + b) / c)")     // (a + b) / c = 5
}

if let a = a, let b = b, var c = c, c != 0 {
    print("(a + b) / c = \((a + b) / c)")     // (a + b) / c = 5
}
```

*** 


## Trailing Closure

Closures that are the last argument of a function should be passed into the function using [trailing closure](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Closures.html#//apple_ref/doc/uid/TP40014097-CH11-ID94) syntax.

*Preferred*

```swift
reversed = names.sort { s1, s2 in return s1 > s2 }
```

*Not Preferred*

```swift
reversed = names.sort({ s1, s2 in return s1 > s2 })
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
