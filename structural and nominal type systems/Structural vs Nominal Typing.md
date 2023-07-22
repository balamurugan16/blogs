The age of preferring dynamically typed languages is changing right now. People start to lean over languages like TypeScript, Go, Rust over languages like Python, Ruby and JavaScript. I am not here to spread hatred on dynamically typed languages, they are excellent in their own ways but when it comes to my personal choice, I would choose Statically typed languages any day even though they would be a pain in the ass to work with (sometimes).

When it comes to Static type system, one key attribute is whether they follow structural or nominal typing. Let me give an example and explain either of them.

### Structural typing
Look at the example below in TypeScript (It follows structural typing BTW)
```ts
type Car = {
  name: string;
}

type Bike = {
  name: string;
}

const myCar: Car = {
  name: "Fortuner"
}

const myBike: Bike = myCar;
```
In the above example, TypeScript won't give any errors when we assign a variable of type Car to a variable of type Bike. Because even though the names of the type definitions are different, The shape of the types are not. Both has a property name of type string. Classes and interfaces in TypeScript will also have the same behavior. 

## Nominal typing
Look at the example below in Java (It follows nominal typing)
```java
class Car {
    String name;
}

class Bike {
    String name;
}

public class Program
{
    public static void main(String[] args) {
        Car car = new Car();
        car.name = "Fortuner";
        
        Bike bike = car;
    }
}
```
In the above example, Java will point out the incompatible types because they are of different type even though the shape of the type is the same.

## Pros and Cons

Structural types gives more flexibility. It follows the pattern of [Duck typing](https://en.wikipedia.org/wiki/Duck_typing), which is "If it walks like a duck and it quacks like a duck, then it must be a duck!". Structural typing also provides the same level of security as nominal typing. 

Nominal types have their own use cases. Languages like C++ and Java has nominal type system. It often times requires a lot of boilerplate code to achieve all sorts of relationships that exists to make it work. 

> That's it folks. Knowing these minute details about the tools that you are using will give you a slight edge over others and my job would be coming up with such content with my blogs.