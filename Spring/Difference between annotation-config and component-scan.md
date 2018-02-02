**What is the difference between annotation-config and component-scan?**

    <context:annotation-config />
or

    @AnnotationDrivenConfig
	

Activates all annotations in beans which are already registered in the application context. Those beans could be defined with XML or by package scanning. 


----------


    <context:component-scan>
or

    @ComponentScan

   Not only does everything that `annotation-config` does, but also registers the java classes as a bean which are annotated with `@Component`, `@Service`, `@Repository` etc.

So without this annotations `@Autowired`  won't work. Without second annotation `@Component`, `@Service` etc annotations won't work.
