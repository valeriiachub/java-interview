
## What is BeanFactoryPostProcessor?  
It's an interface in Spring Core which allows us to modify bean definition before any bean will be instantiated.

**Why do we need it?**
We need this when we want to add additional logic for IoC to create our beans. Suppose you create an annotation and you want Spring to understand it and act accordingly. The BeanPostProcessor is perfect for the purpose.

**How to write your own BeanPostProcessor?**

In order to write our own `BeanFactoryPostProcessor` we need:
1. Create class which implements the interface. You have to override the following method:
`void postProcessBeanFactory(ConfigurableListableBeanFactory beanFactory) throws BeansException;`
	You have access to beanFactory which means you can get bean definition and work with it.
2. Tell Spring about the `BeanFactoryPostProcessor`(`@Bean` or declare the bean in `context.xml`).
