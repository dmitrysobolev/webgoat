# Introduction #

The following instructions will assist developers with building the WebGoat project as well specifying guidelines for contributing to the source code.

## Java source code formatting: ##

WebGoat uses the Eclipse Editor with JavaStyle formatting.  The JavaStyle WebGoat XML file is located at [JavaStyle\_WebGoat.xml](http://code.google.com/p/webgoat/source/browse/trunk/webgoat/main/project/config/JavaStyle_WebGoat.xml).

After building your Eclipse Project using the instructions at [How to Build Webgoat](http://webgoat.googlecode.com/svn/trunk/webgoat/main/HOW%20TO%20create%20the%20WebGoat%20workspace.txt)
  * Right click on the WebGoat project in the package explorer view
    * Select Java Code Style -> Formatter
    * Enable Project Specific Settings
    * Import -> Browse to config/JavaStyle\_WebGoat.xml
    * OK

## Rules of the code base: ##

WebGoat uses the 'The Branch-When-Needed' software management system as identified in the [subversion best practices document](http://svn.collab.net/repos/svn/trunk/doc/user/svn-best-practices.html).

Users commit their day-to-day work on /trunk.
```
    Rule #1: /trunk must compile and pass regression tests at all times.
             Committers who violate this rule are publically humiliated. 
    Rule #2: a single commit (changeset) must not be so large so as to
             discourage peer-review. 
    Rule #3: if rules #1 and #2 come into conflict (i.e. it's impossible
             to make a series of small commits without disrupting the
             trunk), then the user should create a branch and commit a
             series of smaller changesets there. This allows peer-review
             without disrupting the stability of /trunk.
```
Pros: /trunk is guaranteed to be stable at all times.
> The hassle of branching/merging is somewhat rare.

Cons: Adds a bit of burden to users' daily work: they
> must compile and test before every commit.