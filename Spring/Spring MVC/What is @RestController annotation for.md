**What is @RestController annotation for?**
Spring 4.0 introduced `@RestController`, a specialized version of the controller which is a convenience annotation that does nothing more than add the `@Controller` and `@ResponseBody` annotations. 

By annotating the controller class with `@RestController` annotation, you no longer need to add `@ResponseBody` to all the request mapping methods.