# 4 Pillars of Object Orientated Programming (OOP)

## Defintions

Object - a thing or entity. Pretty much anything can be represented as an object, e.g., a car, a bank account, a credit card transaction, etc.

Class - a blueprint for how to create an object. 

Classes contain:

* Data members and functions (C++), or
* Properties and methods (Swift), or
* Fields and procedures

* All of these things mean the same thing, there's just different terminology depending on the language

An object is an instance of a class. The process of creating a class is called instantiation.

</br>
</br>

Constructor - 

Destructor -




# 1. Abstraction

Hide complexity/implementation details. Abstraction allows us to make things that simple to understand and reusable.

Ex:

```C++
area = r1.width * r1.height

vs

area = r1.getArea()
```

# 2. Encapsulation

Make data members of a class private and introduce getters and setters. Getters and setters allow you to have more control of the data. Ex:

```C++
String getSSN() {
    return "XXX-XX-" + ssn.substring(5);
}
```

allows you to hide the full string. Or,

```C++
void setSSN(string s) {
    if (s.length() < 9) return;

    if (!isDigit(s)) return;

    ssn = s;
}
```

allows us to add input validation, preventing the `ssn` property from being assigned a dangerous, invalid value.

Information hiding - information should be hidden from clients, so that a design can be changed without having to rewrite the public methods the client calls to interact with the class.

# 3. Inheritance

Reduce redundant code by creating a generic class that can be inherited. There's a base class (parent class) and subclasses (child classes, or derived classes). A subclass inherits the public and protected data members and functions declared in the base class. **NOTE:** it does not inherit the base class's constructor or destructor.

Subclasses can override functions from the base class. 

In C++, multiple inheritance is allowed, so a class can inherit from more than one class. This isn't a feature in every programming language though.

</br>

In C++, you don't need to call the default constructor of the base class inside of the subclass, unless the base class constructor has parameters. In that case, you can call the constructor explicitly:

```C++
class Rectangle : public Shape {

public:

    Rectangle(Color color) : Shape(color) {
        ...
    }
};
```

</br>

Abstract class - a class that cannot be instantiated.

Concrete classes -

# 4. Polymorphism

