**What are types of IoC container?**
There are two types of IoC container:

 1. **Bean Factory container** - This is the simplest container providing basic support for DI .The BeanFactory is usually preferred where the resources are limited like mobile devices or applet based applications.
 2. **Spring ApplicationContext Container** ? This container adds more enterprise-specific functionality such as the ability to resolve textual messages from a properties file and the ability to publish application events to interested event listeners.

**Annotation based dependency Injection is not supported by BeanFactory** whereas ApplicationContext supports using annotation @PreDestroy, @Autowired.