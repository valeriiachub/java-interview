**What is Dependency Injection?**
**Dependency injection** is a technique whereby one object supplies the dependencies of another object.

An injection is the passing of a dependency to a dependent object(a client) that would use it.

The intent behind dependency injection is to **decouple objects to the extent that no client code has to be changed simply because an object it depends on needs to be changed to a different one**.

Dependency injection is one form of the broader technique of inversion of control. As with other forms of inversion of control, dependency injection supports the dependency inversion principle. The client delegates the responsibility of providing its dependencies to external code (the injector). **The client is not allowed to call the injector code**.