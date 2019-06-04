# servlets accessibility compliance JSP page
Servlets as written in Java are platform independent. 

## Build Commands
```
ant war
```

### Prerequisites
```
Java      1.8
Servlers  3
JSP       2.2
ANT       1.9.14
Tomcat    7
Bootstrap 4.2.1
Jquery    3.3.1
```
## Configure the Application Deployment Descriptor - "web.xml"
A web user invokes a servlet, which is kept in the web server, by issuing a specific URL from the browser. In this example, we shall configure the following request URL to trigger the "home.jsp":
```
<?xml version="1.0" encoding="UTF-8"?>
<web-app xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://java.sun.com/xml/ns/javaee" xsi:schemaLocation="http://java.sun.com/xml/ns/javaee http://java.sun.com/xml/ns/javaee/web-app_3_0.xsd" id="WebApp_ID" version="3.0">
  <display-name>ConduentDemo</display-name>
  <servlet>
    <description></description>
    <servlet-name>HomePageServletController</servlet-name>
    <servlet-class>conduentdemo.controllers.HomePageServlet</servlet-class>
  </servlet>
  <servlet-mapping>
    <servlet-name>HomePageServletController</servlet-name>
    <url-pattern>/homePageClick</url-pattern>
  </servlet-mapping>
  <welcome-file-list>
    <welcome-file>home.jsp</welcome-file>
  </welcome-file-list>
</web-app>
```
### Run the JSP Servelt
To run the servlet, first start the Tomcat server. deployee the generated the war in WebApp folder 
