![http://webgoat.googlecode.com/svn/trunk/webgoat/src/main/webapp/images/header/header.jpg](http://webgoat.googlecode.com/svn/trunk/webgoat/src/main/webapp/images/header/header.jpg)
# WebGoat 6.0 Has Started - Help Still Wanted #
After 1,000,000+ downloads and 10+ years, we have started an effort to significantly upgrade **WebGoat**. We are looking for help.
If you have experience in **any** of these areas and time to contribute:
  * UI Design
  * Spring MVC
  * JavaEE
  * ESAPI and other security controls
  * Application attacks (lessons revamp)
  * Technical writing
Please contact Bruce Mayhew (webgoat AT owasp DOT org).

# WebGoat has moved to github #
The source code repository has moved to github,  You can find us at  https://github.com/webgoat

There are many WebGoat repositories on GitHub.  [This](https://github.com/webgoat) is the official one.  Even the repository at https://github.com/OWASP/webgoat is not the official repository.

# Overview #
**WebGoat** is a deliberately insecure J2EE web application designed to teach web application security lessons. In each lesson, users must demonstrate their understanding of a security issue by exploiting a real vulnerability in the WebGoat application. For example, in one of the lessons the user must use SQL injection to steal fake credit card numbers. The application is a realistic teaching environment, providing users with hints and code to further explain the lesson.

Why the name 'WebGoat'? Developers should not feel bad about not knowing security. Even the best programmers make security errors. What they need is a scapegoat, right? Just blame it on the 'Goat!

## Goals ##

Web application security is difficult to learn and practice. Not many people have full blown web applications like online book stores or online banks that can be used to scan for vulnerabilities. In addition, security professionals frequently need to test tools against a platform known to be vulnerable to ensure that they perform as advertised. All of this needs to happen in a safe and legal environment. Even if your intentions are good, we believe you should never attempt to find vulnerabilities without permission.

The primary goal of the WebGoat project is simple: create a de-facto interactive teaching environment for web application security. In the future, the project team hopes to extend WebGoat into becoming a security benchmarking platform and a Java-based Web site Honeypot.

## Questions ##

If you have questions or suggestions regarding WebGoat, send email to Bruce Mayhew at "webgoat AT owasp DOT org"

## Special Release Notices for Ubuntu ##

April-28-2012: The Ubuntu release had some issues with the JRE and was removed.  A new version will be posted soon.


## Releases ##

WebGoat 5.4 is mainly a bug-fix release.

[WebGoat installation instructions](http://code.google.com/p/webgoat/wiki/Installation)

#### WebGoat 5.4 Standard: ####
The standard release is a download, unzip, and click-to-run release.  It comes with the Java Runtime Environment and a configured Tomcat 7 server.  There are versions for 32 bit Windows and Ubuntu.

#### WebGoat 5.4 Developer : ####

As of version 5.3, WebGoat now uses maven.  See the [readme](http://webgoat.googlecode.com/files/README-5.4.txt) file for instructions on how to build and setup an eclipse environment.

## How did I do that ##
References to interesting articles on WebGoat.  Contact Bruce Mayhew at webgoat AT owasp DOT org" if you have a detailed post.
  * [Creating a OWASP WebGoat Ubuntu-based VM](http://vwelch.blogspot.com/2009/04/creating-owasp-webgoat-ubuntu-based-vm.html)
  * [Developing Secure Applications](http://www.datamanager.it/cms/view/sezioni_web/english_contents/developing_secure_applications/s162/c80840)
  * [Securing WebGoat using OWASP ModSecurity Project](http://www.owasp.org/index.php/Category:OWASP_Securing_WebGoat_using_ModSecurity_Project)
  * [Black Hat - Securing WebGoat using OWASP ModSecurity](http://www.owasp.org/images/5/59/Virtual_Patching_Ryan_Barnett_Blackhat_Federal_09.zip)
## External Documentation ##
References to WebGoat documentation or solutions.
  * [WebGoat on YouTube](http://www.youtube.com/results?search_query=webgoat&oq=webgoat&aq=f&aqi=g4)
  * [WebGoat Solution Movies](http://yehg.net/lab/pr0js/training/webgoat.php)
  * [WebGoat solutions in French](http://www.aldeid.com/index.php/OWASP_WebGoat)