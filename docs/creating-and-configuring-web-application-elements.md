[//]: # (Source: https://www.jetbrains.com/help/idea/creating-and-configuring-web-application-elements.html)
[//]: # (Downloaded: 2025-12-17 19:23:15)

## Define templates for Web application elements

IntelliJ IDEA does not provide the default templates for creating servlets, listeners, and filters. However, you can define these templates yourself.

[Servlets](https://docs.oracle.com/javaee/5/tutorial/doc/bnafe.html) as a part of a Web application are created and configured through the `<servlet>` and `<servlet-name>` elements in the web.xml Web Application deployment descriptor.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | File and Code Templates.

  2. On the Files tab, click ![Create Template](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to create a new file template.

  3. Name the new template `Servlet` and specify `Servlet` as the file name. Make sure that the extension is `java`.

  4. Paste the following code as the template body:

#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end #parse("File Header.java") import javax.servlet.*; import javax.servlet.http.*; import javax.servlet.annotation.*; import java.io.IOException; @WebServlet(name = "${Class_Name}", value = "/${Class_Name}") public class ${Class_Name} extends HttpServlet { @Override protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException { } @Override protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException { } }

  5. Apply the changes and close the dialog.


![Defining template for Filter Web application element](https://resources.jetbrains.com/help/img/idea/2025.3/web-element-servlet-template.png)

The Servlet element defines the name of the servlet and specifies the compiled class that implements it. Alternatively, instead of specifying a servlet class, you can specify a JSP.

The Servlet element also contains definitions of initialization attributes.

Note that you can map URL pattern that associates the servlet with the set of URLs that call the servlet using annotations in the editor.

A listener receives notifications on any events related to the Web application, such as deployment/undeployment of the Web application, activation/deactivation of an HTTP session, as well as on adding, removing, and replacing attributes of the application/session.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | File and Code Templates.

  2. On the Files tab, click ![Create Template](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to create a new file template.

  3. Name the new template `Listener` and specify `Listener` as the file name. Make sure that the extension is `java`.

  4. Paste the following code as the template body:

#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end #parse("File Header.java") import javax.servlet.*; import javax.servlet.http.*; public class ${Class_Name} implements ServletContextListener, HttpSessionListener, HttpSessionAttributeListener { public ${Class_Name}() {} @Override public void contextInitialized(ServletContextEvent sce) { /* This method is called when the servlet context is initialized(when the Web application is deployed). */ } @Override public void contextDestroyed(ServletContextEvent sce) { /* This method is called when the servlet Context is undeployed or Application Server shuts down. */ } @Override public void sessionCreated(HttpSessionEvent se) { /* Session is created. */ } @Override public void sessionDestroyed(HttpSessionEvent se) { /* Session is destroyed. */ } @Override public void attributeAdded(HttpSessionBindingEvent sbe) { /* This method is called when an attribute is added to a session. */ } @Override public void attributeRemoved(HttpSessionBindingEvent sbe) { /* This method is called when an attribute is removed from a session. */ } @Override public void attributeReplaced(HttpSessionBindingEvent sbe) { /* This method is called when an attribute is replaced in a session. */ } }

  5. Apply the changes and close the dialog.


![Defining template for Filter Web application element](https://resources.jetbrains.com/help/img/idea/2025.3/web-element-listener-template.png)

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | File and Code Templates.

  2. On the Files tab, click ![Create Template](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to create a new file template.

  3. Name the new template `Filter` and specify `Filter` as the file name. Make sure that the extension is `java`.

  4. Paste the following code as the template body:

#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end #parse("File Header.java") import javax.servlet.*; import javax.servlet.annotation.*; @WebFilter(filterName = "${Class_Name}") public class ${Class_Name} implements Filter { public void init(FilterConfig config) throws ServletException { } public void destroy() { } @Override public void doFilter(ServletRequest request, ServletResponse response, FilterChain chain) throws ServletException, IOException { chain.doFilter(request, response); } }

  5. Apply the changes and close the dialog.


![Defining template for Filter Web application element](https://resources.jetbrains.com/help/img/idea/2025.3/web-element-filter-template.png)
