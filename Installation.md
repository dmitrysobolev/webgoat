# Introduction #

WebGoat installations are intended to be download, unzip, and click-to-run installations.  However, some users prefer just downloading the war file.  Instructions for all installations are included.


# Details #

## WebGoat Standard Releases ##

This release comes with a JRE and Tomcat 7.

  * Download WebGoat-X.X-OWASP\_Standard\_Win32.zip or WebGoat-X.X-OWASP\_Standard\_Ubuntu32 from [WebGoat Downloads](http://code.google.com/p/webgoat/downloads/list)
  * Extract the file to a WebGoat root directory of your choosing
    * The WebGoat zip file has a WebGoat-X.X root folder
  * Change directory to WebGoat-X.X directory
  * Double-click the webgoat.bat for Windows or run ./webgoat.sh start8080 for Ubuntu
    * A Tomcat window will start
  * Browse to http://localhost/WebGoat/attack for Windows or http://localhost:8080/WebGoat/attack for Ubuntu
  * Username = guest, password = guest

## WebGoat Developer Releases ##

Version 5.4 uses maven, see the readme for instructions


## WebGoat War File Releases ##

This release assumes either a previous installation of a WebGoat Standard release or the host machine has Java 1.6 or higher and Tomcat 7.  If you have not installed the Standard release, you will need to modify the tomcat/conf/tomcat-users.xml file to add the WebGoat users.  See the [FAQ](http://code.google.com/p/webgoat/wiki/FAQ)
  * Download WebGoat-X.X.war from [WebGoat Downloads](http://code.google.com/p/webgoat/downloads/list)
  * Shutdown Tomcat if running - just close the tomcat window
  * Copy the war file to WebGoat-X.X\tomcat\webapps\WebGoat.war
  * Delete the existing WebGoat-X.X\tomcat\webapps\WebGoat directory
    * **This will cause all lesson status to be lost**
    * To save lessons status, copy the webapps\WebGoat\users folder
    * Restore the users directory **after** you restart WebGoat
  * Change directory to WebGoat-X.X directory
  * Double-click the webgoat.bat for Windows or run ./webgoat.sh start8080 for Ubuntu
    * A Tomcat window will start
  * Browse to http://localhost/WebGoat/attack for Windows or http://localhost:8080/WebGoat/attack for Ubuntu
  * Username = guest, password = guest

