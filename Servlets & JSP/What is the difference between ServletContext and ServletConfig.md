## What is the difference between ServletContext and ServletConfig?

**Servlet Config**  

 - `ServletConfig` object is one per servlet class.
 - Object will be created for during initialization process of the servlet.
 - In web.xml - `<init-param>` tag will be appeared.

> **web.xml**

    <servlet>
        <servlet-name>ServletConfigTest</servlet-name>
        <servlet-class>com.stackoverflow.ServletConfigTest</servlet-class>
        <init-param>
            <param-name>topic</param-name>
            <param-value>ServletConfig vsServletContext</param-value>
        </init-param>
    </servlet>

`GenericServlet` has `ServletConfig config` field and 

    public ServletConfig getServletConfig() {
    	return config;
    }

So in our servlet we can get the config(for example, in doGet() method):
   
     ServletConfig servletConfig = getServletConfig();


----------
**Servlet Context**

 - ServletContext object is global to entire web application
 - Object of ServletContext will be created at the time of web application deployment
 - In web.xml - `<context-param>` tag will be appear.

> **web.xml**

    <context-param>
        <param-name>globalVariable</param-name>
        <param-value>com.stackoverflow</param-value>
    </context-param>

`GenericServlet` has `ServletContext context` field and 

    public ServletContext getServletContext() {
        ServletConfig sc = getServletConfig();
        if (sc == null) {
            throw new IllegalStateException(
                lStrings.getString("err.servlet_config_not_initialized"));
        }
    
        return sc.getServletContext();
    }

So in our servlet we can get the config(for example, in doGet() method):
   
     ServletContext servletContext = getServletContext();