Releasepack: Java
=========================

This is a "release pack" for java applications.

What's a release pack?
----------------------

A release pack is like a [buildpack](http://devcenter.heroku.com/articles/buildpack), but it's not responsible for actually compiling applications.  It operates on a directory with the applicaiton already built, and its job is to download auxiliary software like runtime environments (in this instance, a java JDK) and place them in the appropriate directory under the build root.

A release pack can also set up default instance type entires in a Procfile, however this release pack doesn't do this.

Choose a JDK
--------------
Create a `system.properties` file in the root of your project directory and set `java.runtime.version=1.7`.

Example:

    $ cat Procfile 
    app.jar
    
    $ echo "java.runtime.version=1.7" > system.properties
