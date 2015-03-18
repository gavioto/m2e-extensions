# Overview #
Eclipse Plugin providing extensions for [M2Eclipse](http://m2eclipse.sonatype.org/) (Maven Integration for Eclipse). By extensions we mean _project configurators_ for the m2eclipse Eclipse plugin.

## Features ##
_m2eclipse_ provides extension points to add functionality to the plugin itself. _m2e-extensions_ eclipse plugin provides implementation for automatically configuring various Eclipse Plugins when a Maven project is imported or configured by reading the corresponding **maven plugin** configuration in the _pom.xml_. Currently the m2e-extensions supports configuring the following Eclipse plugins:

  * eclipse-cs (Eclipse Checkstyle plugin), this plugin will be configured by reading the [maven-checkstyle-plugin](http://maven.apache.org/plugins/maven-checkstyle-plugin/checkstyle-mojo.html) configuration from pom.xml.

  * PMD for eclipse (Eclipse PMD plugin), this plugin will be configured by reading the [maven-pmd-plugin](http://maven.apache.org/plugins/maven-pmd-plugin/pmd-mojo.html) configuration from pom.xml.

  * Findbugs for eclipse (Eclipse FindBugs plugin), this plugin will be configured by reading the [findbugs-maven-plugin](http://mojo.codehaus.org/findbugs-maven-plugin/findbugs-mojo.html) configuration from pom.xml.

## Installation ##

Please see the [installation](Installation.md) page.
