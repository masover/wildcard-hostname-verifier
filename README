# Wildcard Hostname Verifier for Oracle WebLogic

## Insiration

I had the same need as [this guy](http://jandrewthompson.blogspot.com/2010/04/weblogic-and-wildcard-ssl-certificates.html), but I don't trust regex hackery for something this sensitive. This is my attempt -- no external dependencies (though I really should've used antlr), and an attempt to stay as close to RFC2253 as I can.

## Installation

[Download the jar][download] and put it somewhere in WebLogic's CLASSPATH. This must be the CLASSPATH for an entire server, not just your application. To try it out in JDeveloper's Integrated WebLogic server, you have very little choice -- mine is here:

    Oracle/Middleware/patch_wls1033/profiles/default/sys_manifest_classpath/weblogic_patch.jar

Watch out when you patch WebLogic, though. I have no idea how it interacts with actual WebLogic patches.

## Deployment

[Download the jar][download], and install it somewhere in your server's classpath. Then follow Oracle's directions on [configuring a custom hostname verifier](http://download.oracle.com/docs/cd/E12840_01/wls/docs103/ConsoleHelp/taskhelp/security/ConfigureACustomHostNameVerifier.html). Set the Custom Hostname Verifier to:

    net.forkbox.weblogic.WildcardHostnameVerifier

## Building/Hacking

This is set up as an Eclipse project because Java demands an IDE, but I've also built an ant buildfile, both because this is how Eclipse builds jars, and because it should lower the barrier of entry.

So to build: Install ant, then run 'ant' in a shell. You should get a jar. You can now install as above.

  [download]: http://github.com/masover/wildcard-hostname-verifier/downloads
