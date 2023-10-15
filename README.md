# JavaSE-Packages and Modules

In Java, "packages" and "modules" are both used for organizing and structuring code, but they serve slightly different purposes.

## 1. Packages

A package in Java is a way to organize related classes and interfaces into a single directory hierarchy. 

It helps in avoiding naming conflicts and provides a way to group related code together. Here's a simple example:

```java
// File: MyPackageExample.java
package com.example.mypackage;

public class MyClass {
    public void display() {
        System.out.println("Hello from MyClass!");
    }
}
```

In this example, the MyClass is part of the com.example.mypackage package.

## 2. Modules

Java 9 introduced the concept of modules to enhance modularity in the language. A module is a collection of packages. 

It encapsulates code and data, providing a way to hide the implementation details of a module and only expose the necessary parts. Here's a basic example:

```java
// File: module-info.java
module mymodule {
    exports com.example.mypackage; // Exports the package for other modules to use
}
```

In this example, the mymodule module exports the com.example.mypackage package, allowing other modules to access the classes within that package.

Remember, Java modules offer stronger encapsulation compared to packages, as they allow you to control which parts of your code are visible outside the module.
