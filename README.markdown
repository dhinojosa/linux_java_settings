#Making Java Swing and IntelliJ better looking in Linux

This project merely holds personal settings of my JDK (6.0) in a Linux environment.

1. Install the free true type font set `sudo apt-get install ttf-freefont`
2. `fontconfig.properties` and `fontconfig.Ubuntu.properties` should go into the `$JAVA_HOME/jre/lib/` directory.  If `JAVA_HOME` is not set, you can export by including in your .bashrc: `export JAVA_HOME=<jdk location>`.
3. For better Java application font rendering add the following command line arguments: `-Dswing.aatext=true -Dawt.useSystemAAFontSettings=on`.  For IntelliJ include these lines in `<intellij_home>/bin/idea.vmoptions`

**Note: As of JRE 7, Linux no longer uses `fontconfig.*` to determine what fonts to display, it instead uses system settings.  That's good since we no longer need to use `xfontsel` but it is still ugly in Linux**
