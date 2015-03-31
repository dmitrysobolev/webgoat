Before contacting webgoat support at webgoat at owasp.org or posting to the [WebGoat mailing list](http://lists.owasp.org/mailman/listinfo/owasp-webgoat), please read the FAQ to see if your question may have been answered.
#  #

---

#  #
**Q. How do I report a bug?**
#  #
**A.** Add your bug to the [WebGoat Issues](http://code.google.com/p/webgoat/issues/list) page.

**----------------------------------------------------------------------------------------**

**Q. I put the WebGoat war file in my tomcat/webapps directory and the http://localhost/WebGoat/attack URL doesn't work.**
#  #
**A.** Rename the downloaded war file to WebGoat.war.  Delete the existing tomcat/webapps/**WebGoat** directories. Restart Tomcat.

**----------------------------------------------------------------------------------------**

**Q. I dropped the WebGoat war file into my non-Tomcat application server and WebGoat doesn't seem to work.**
#  #
**A.** WebGoat uses Basic Authentication.  The users and roles are defined in tomcat/conf/tomcat-users.xml.  These same users and roles must be added to your application server.

**----------------------------------------------------------------------------------------**

**Q. Having problems with the ant file working properly. How do I configure my ant environment so that I don't receive errors such as:
> - "Specified VM install not found: type Standard VM, name j2sdk1.4.2.06"**
#  #
**A.** This usually indicates an Eclipse environment setting misconfiguration. Here are some possible solutions:
```
	 Ant Runtime Configuration
		- Window > Preferences
		- Ant > Runtime
		- Under Classpath Tab check the "Global Entries"
		- Remove any jre "tools.jar" references
		- Add the "\tomcat\servers\lib\catalina-ant.jar" file.
		- Click Apply, Click OK.
		- Return to the Ant View and refresh.
```

**----------------------------------------------------------------------------------------**

**Q. When I start up WebGoat it dies very quickly.**
#  #
**A.** WebGoat is a Java application that runs on Tomcat using port 80.  If you have another application listening on port 80 (like IIS), you will need to change WebGoat's port (to 8080 or something) in the tomcat\_root/conf/server.xml file.  You can also start up webgoat using the webgoat\_8080.bat file.  You will then need to browse to:
> http://localhost:8080/WebGoat/attack

**----------------------------------------------------------------------------------------**

**Q. When I deploy the war file to the Tomcat wepapps directory, I can't login to WebGoat**
#  #
**A.** You need to add the webgoat users and roles to tomcat/conf/tomcat-users.xml
```
    <?xml version="1.0" encoding="UTF-8"?>
    <tomcat-users>
      <role rolename="webgoat_basic"/>
      <role rolename="webgoat_admin"/>
      <role rolename="webgoat_user"/>
      <role rolename="tomcat"/>
      <user password="webgoat" roles="webgoat_admin" username="webgoat"/>
      <user password="basic" roles="webgoat_user,webgoat_basic" username="basic"/>
      <user password="tomcat" roles="tomcat" username="tomcat"/>
      <user password="guest" roles="webgoat_user" username="guest"/>
    </tomcat-users>
```

**----------------------------------------------------------------------------------------**

**Q. How do I get configure WebGoat to run on an IP other then localhost?**
#  #
**A.** In the webgoat.bat file, in the root directory, the following lines are executed:
```
      delete .\tomcat\conf\server.xml 
      copy .\tomcat\conf\server_80.xml .\tomcat\conf\server.xml 
```
> This will overwrite any changes you may have made to server.xml file that addressed this issue....

> By changing the server\_80.xml file (or by removing the above code from webgoat.bat, after making your changes) you can reflect your changes to the Tomcat configuration. You will need to change the IP address in the server\_80.xml file to be the IP of the host machine.

> The following connectors should be modified
```
      <!-- Define a non-SSL HTTP/1.1 Connector on port 8080 --> 
      <Connector address="10.20.20.123" port="80" 
      ... 
      <!-- Define a SSL HTTP/1.1 Connector on port 8443 --> 
      <Connector address="10.20.20.123" port="443" 
      .... 
```
> where the 127.0.0.1 will be replaced by your IP. In this case 10.20.20.123

**----------------------------------------------------------------------------------------**

**Q. How do I solve lesson X?**
#  #
**A.** Subscribe to the WebGoat mailing list at owasp-webgoat@lists.owasp.org.
> Post your question to owasp-webgoat@lists.owasp.org

**----------------------------------------------------------------------------------------**

**Q. How do I report a bug?**
#  #
**A.** Add your bug to the [WebGoat Issues](http://code.google.com/p/webgoat/issues/list) page.