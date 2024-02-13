# JavaSE-Packages and Modules

See the Udemy course: https://www.udemy.com/course/curso-certificacion-profesional-desarrollador-java-se-11

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

## 3. Deeper in Packages and Modules in Java

Let's delve a bit deeper into packages and modules in Java.

### Packages

1. Purpose:

Organization: Packages help organize Java code into a hierarchical structure. They prevent naming conflicts by providing a namespace for the classes.

Access Control: They also help in access control by using the public, protected, package-private (default), and private modifiers.

2. Example:

In the previous example, com.example.mypackage is a package. It's like a folder structure for your classes.

3. Access Modifiers:

Classes, interfaces, and members within a package have package-private access by default.

Classes and interfaces can also have public or protected access within a package.

4. Import Statements:

To use classes from another package, you use import statements. For example:

```java
import com.example.mypackage.MyClass;
```

5. Directory Structure:

Packages map to directory structures. The com.example.mypackage would correspond to a directory structure like com/example/mypackage.

### Modules

1. Purpose:

Strong Encapsulation: Modules provide a higher level of encapsulation compared to packages. You can specify which packages are visible to other modules and which are not.

Dependency Management: Modules help manage dependencies by explicitly declaring what other modules they depend on.

2. Example:

In the module example, mymodule is a module. It encapsulates the package com.example.mypackage and exports it for other modules to use.

3. module-info.java:

Each module has a file named module-info.java that declares the module's name, dependencies, and what packages are exported or opened to other modules.

```java
module mymodule {
    exports com.example.mypackage;
}
```

4. Access Modifiers in Modules:

Modules have access modifiers like exports and opens to control what is accessible from the outside.

5. Module Path:

In Java, there's a module path alongside the classpath. It is used to specify where to find modules. The module path can include both modular JAR files and directories containing modules.

6. Module Declarations:

Modules declare dependencies on other modules, which helps in maintaining a clear understanding of the project structure.

7. Benefits:

Better encapsulation: Modules provide stronger encapsulation, reducing the risk of unintended dependencies.

Improved maintainability: Clear module declarations enhance project maintainability and make it easier to reason about dependencies.

Both packages and modules contribute to code organization, but modules take it a step further by offering enhanced encapsulation and dependency management. 

They're particularly useful in large-scale projects where managing complexity is crucial.
