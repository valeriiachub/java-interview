## Describe options for creating ApplicationContext  

 - `AnnotationConfigApplicationContext`
		For the apps when we configure out context via annotations.
- `ClassPathXmlApplicationContext`
	 For the apps when we configure our context via annotations.
- `FileSystemXmlApplicationContext`
	Similar to `ClassPathXmlApplicationContext`  but now our xml file can be located not only in classpath but also in entire file system.
- `GenericGroovyApplicationContext`
	For groovy based configuration.
- `WebApplicationContext`
 Spring MVC application context which has acess to `ServletContext`.
