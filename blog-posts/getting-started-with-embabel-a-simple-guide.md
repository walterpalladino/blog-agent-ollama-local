# Getting Started with Embabel: A Simple Guide

## What is Embabel?

Embabel is a lightweight tool that helps you embed runnable code examples in your documentation. Write your code once, then run it directly from your docs.

This is useful for tutorials and API guides. Readers can see working code right away.

## Why Use Embabel?

Traditional documentation has static code snippets. Readers must copy, paste, and run them manually. Embabel solves this problem by making your examples executable. Readers learn faster and authors save time.

## Setup with Maven

Add Embabel to your Maven project by opening your `pom.xml` file and adding this dependency:

```xml
<dependency>
    <groupId>com.embabel</groupId>
    <artifactId>embabel-core</artifactId>
    <version>1.0.0</version>
</dependency>
```

Download the library by running:

```bash
mvn clean install
```

## A Simple Example

Let's create a basic Java class and use Embabel to make it runnable.

```java
import com.embabel.Embabel;
import com.embabel.Runner;

public class HelloWorld {
    public static void main(String[] args) {
        Runner runner = Embabel.createRunner();
        runner.run(() -> {
            System.out.println("Hello from Embabel!");
        });
    }
}
```

Running this class produces:

```
Hello from Embabel!
```

## How It Works

Embabel uses a simple pattern. You wrap your code in a lambda, and the Runner executes it. This makes your code portable.

The key parts are:

1. **Embabel.createRunner()** - creates a runner object
2. **runner.run()** - executes your lambda
3. **Lambdas** - hold your executable code

## A More Realistic Example

Here is a service class:

```java
public class UserService {
    public String greetUser(String name) {
        return "Hello, " + name + "!";
    }
}
```

Run it with Embabel:

```java
public class Main {
    public static void main(String[] args) {
        UserService service = new UserService();
        
        Runner runner = Embabel.createRunner();
        runner.run(() -> {
            String message = service.greetUser("Alex");
            System.out.println(message);
        });
    }
}
```

Output:

```
Hello, Alex!
```

## Benefits for Your Project

- Documentation stays current
- Code examples are always tested
- Readers can copy with confidence
- Less work for technical writers

## Conclusion

Embabel makes your documentation come alive. It is simple to learn and integrates easily with Maven. Try it in your next Java project.

Your readers will thank you!