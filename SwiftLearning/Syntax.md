
//Tut 1
var str = "Hello World"
print(str)

var a = 2
var b = 1

a = button
str = 29

var numberOfApples = 19

print(a+b)
print(a-b)
print(a*b)
print(a/b)

let c = 10

//Tut 2
var str:String = "Hello, playground"
print(str)

var a:Int = 2
var b:Int = 1

a = b

var c:Float = 2.3
var d:Double = 13.19
var e:Bool = true

print(Int(c))
print(Int(d))
print(Int(round(d)))

var numberOfApples = 19

print(a+b)
print(a-b)
print(a*b)
print(a/b)

let f = 10

//Tut 3 
let a = 1

if a < 4 {
    print("only if a is less than 4")
} else if a < 8 {
    print("only if a is less than 8")
} else {
  print("Nothing was true")  
}

//Tut4

var someCharacter:Character = "a"

switch someCharacter{
    case "a":
        print("is an A")
    case "b", "c":
        print("is a B or C")
    default:
        print("some fallback")
}

//Tut5

var str = "Hello, playground"

for index in 1...5 {
    print(index)
}

for _ in 1...5{
    print("hello")
}

//Tut 6

var counter = 5

while counter>0 {
    print("hello")
    counter -= 1
}

repeat {
    print("hello")
    counter -= 1
} while counter > 0

//Tut 7

func addTwoNumbers(using number1:Int , and number2:Int) -> Int{
    return number1+number2
}

let sum = addTwoNumbers(using:1,and:2)

func addTwoNumbers(_ number1:Int , _ number2:Int) -> Int{
    return number1+number2
}

let sum = addTwoNumbers(1,2)

//Tut 8


class BlogPost {
    var title = ""
    var body = ""
    var author = ""
    var numberOfComments = 1
    
    func addComments(){
        numberOfComments+=1
    }
}

let myPost = BlogPost()
myPost.title = "Hello playground"
myPost.author = "Chris Ching"
myPost.body = "Hello"
myPost.addComment()
print(myPost.numberOfComments)

let mySecondPost = BlogPost()
mySecondPost.title = "GoodBye Playground"
mySecondPost.author = "John Travolta"
mySecondPost.body = "Hello"
print(mySecondPost.numberOfComments)

//Tut9

class Car{
    var topSpeed = 200
    func drive() {
        print("Driving at \(topSpeed)")
    }
}

let myRide = Car()
myRide.topSpeed
myRide.drive()


class Futurecar {
    var topSpeed = 250
    
    func drive() {
        print("Driving at \(topSpeed)")
    }
    
    func fly() {
        print("Flying")
    }
}

instead of he above, we can use 

class Futurecar : Car {
    func fly() {
        print("Flying")
    }
}

let myRide = Car()
myRide.topSpeed
myRide.drive()

let myNewRide = Futurecar()
myNewRide.topSpeed
myNewRide.drive()
myNewRide.fly()


Ovverriding

class Futurecar : Car {
    override func drive() {
        super.drive()
        print("and rockets bossting to \(topSpeed+50)")
    }
    
    func fly() {
        print("Flying")
    }
}

//Tut 10

class Person {
    var name = ""
    var age = 10
    
    init() {
        
    }
    
    init(_ name:String, _ age:Int) {
        self.name = name
        self.age = age
    }
}


var a = Person("Chris",33)
var b = Person()

b.name
b.age

// Optionals

class Person{
    var name = ""
}

class BlogPost {
    var title:String?
    var body = "hey"
    var author:Person?
    var numberOfComments = 0
}

let post = BlogPost()

print(post.Body + " hello! ")


//Optional Binding
if let actualTitle = post.title {
    
}

//Forced Unwrapping - when you know it definitely holds values

post.title = "yo"

print(post.title! + " salut")

if post.title != nil{
    print(post.title!+ " salut ")
}

if post.title == nil{
    // Optional contains no value
}



// Properties

Class Person {
    var name = ""
}

Class BlogPost {
    //COMPUTED PROPERTY
    var fullTitle:String {
        
        if title != nil && author != nil {
            return title! + " by " + author!.name
        }
        else if title != nil {
            return title!
        }
        else {
            return "No Title"
        }
    }
    
    Var title:String?
    Var body = "hey"
    Var author:Person?
    Var numberOfComments = 0
}


//force unwrapping lets you use the variale without checks,
//its the job of the initializer to make sure its assigned


class BlogPost{
    var title:String!
    var body = "hey"
    var author:Person!
    Var numberOfComments = 0
}
let post = BlogPost()
post.title //compiler doesnt thrown any error

// howver you cant leave a variable without assigning or ? or ! ,
//if you do do that, you will be forced by compiler to take steps to assign it a value

class BlogPost{
    var title:String
    var body = "hey"
    var author:Person
    var numberOfComments = 0
    
    init()  {
        title = "My Title"
        author = Person()
    }
    
    convenience init(customTitle:String) {
        self.init()
        title = customTitle
    }
}

//Arrays - a collection of data ordered by indexes


var d = ["dog","cat","bird"]

for counter in 0...2 {
    print("my" + d[counter])
}

for item in d {
    print("my " + item)
}

var d = ["dog","cat","bird"]
var e = [String]()

d += ["mouse","owl"] 

d.append(["cat","rat"])

d.remove(at: 0)

d[0] = "turtle"

print(d[0])
d.count


var str = "Hello, playground"

var carDB = Dictionary<String,String>()
var carDB2 = [String:String]()


carDB["JSD 238"]  = "Blue Ferrari"
carDB["SID 482"] = "Green Lamborghini"

cardDB["JSD 238"]

cardDB["JSD 238"] = "Red Ferrari"

cardDB["JSD 238"] = nil

for (license, car) in cardDB {
    print("\(car) has a license : \(license)")
}
