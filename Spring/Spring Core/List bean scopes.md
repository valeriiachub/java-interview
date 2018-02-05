## List bean scopes

Spring supports five scopes(three are available only in web aware `ApplicationContext`):

 1. **singleton**
Only once per Spring container.
Spring's default scope.
 2. **prototype**
New bean created with every request or reference.

	Spring does not manage the complete lifecycle of a prototype bean(destruction). It is responsibility of the client code to clean up prototype scoped objects and release any expensive resources that the prototype beans are holding onto.

	As a rule of thumb, you should use the prototype scope for all beans that are stateful, while the singleton scope should be used for stateless beans.
 3. **request**
New bean per servlet request.
 4. **session**
New bean per session.
 5. **global session**
New bean per global HTTP session(portlet context).