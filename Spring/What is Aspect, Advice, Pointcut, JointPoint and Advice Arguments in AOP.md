**What is Aspect, Advice, Pointcut, JointPoint in AOP?**
**Aspect** is a class that implements enterprise application concerns that cut across multiple classes, such as transaction management. Aspects can be a normal class configured through Spring XML configuration or we can use Spring AspectJ integration to define a class as Aspect using @Aspect annotation.

    @Aspect
    public class EmployeeAspect {
    	...
    }


----------
**Advice** is an action taken by an aspect at a particular join point. Different types of advice include "around," "before" and "after" advice. (Advice types are discussed below.) Many AOP frameworks, including Spring, model an advice as an interceptor, maintaining a chain of interceptors around the join point.


----------
Advice is associated with a pointcut expression, and runs before, after, or around method executions matched by the pointcut.

In simple terms, advice is the method which has annotation like `@Before`, `@After` and others:

      @Before("com.xyz.myapp.SystemArchitecture.dataAccessOperation()")
      public void doAccessCheck() {
        // ...
      }


----------
**Pointcut** are expressions that is matched with join points to determine whether advice needs to be executed or not. Pointcut uses different kinds of expressions that are matched with the join points and Spring framework uses the AspectJ pointcut expression language.

Example is:

    "com.xyz.myapp.SystemArchitecture.dataAccessOperation()"


**Join point** is the specific point in the application such as method execution, exception handling, changing object variable values etc. In Spring AOP a join points is always the execution of a method.