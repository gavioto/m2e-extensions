

# WARNING #
The project configurator has been removed temporarily, due to class loading issues. Working with
the Findbugs Eclipse Team (via and issue ticket) to resolve this.

# Introduction #

<p>
The m2e-extension FindBugs project configurator will read the <i>findbugs-maven-plugin</i> configuration<br>
from the pom.xml and configure the FindBugs Eclipse Plugin. Not, all <i>findbugs-maven-plugin</i> are supported<br>
in the current release as some of these might not be applicable to the FindBugs Eclipse plugin.<br>
</p>

## CAVEATS ##
<p>
Remember if you are using the configurator (unless disabled) it will <b>override</b> any customization of<br>
the FindBugs Eclipse plugin. You should <b>not</b> use the m2e-extensions, if you would like to preserve your<br>
settings.<br>
</p>

## Supported _findbugs-maven-plugin_ elements ##

The following _findbugs-maven-plugin_ configuration elments are supported:

  * _debug_
  * _excludeFilterFile_
  * _includeFilterFile_
  * _threshold_
  * _omitVisitors_
  * _visitors_

## New maven plugin configuration elements ##
<p>
Although the findbugs-maven-plugin does not support this elements, this can be safely put in the<br>
configuration elements, so the FindBugs Eclipse plugin can be configured. Note: this may some day<br>
natively supported in the findbugs-maven-plugin. The elements are:<br>
</p>

  * _priority_
  * _bugCategories_ ( a comma separated list of BugCategories) the bug categories are:
    * CORRECTNESS
    * NOISE
    * SECURITY
    * BAD\_PRACTICE
    * STYLE
    * PERFORMANCE
    * MALICIOUS\_CODE
    * MT\_CORRECTNESS
    * I18N
    * EXPERIMENTAL

## Disabling the configuration ##
<p>
The m2e-extension findbugs project configurator can be disabled completely by adding the following<br>
configuration element. When you do this, the FindBugs Eclipse plugin will not be configured by the m2e-extensions<br>
project configurator. The element name is <i>m2eclipseConfig</i> and the child element <i>disable</i> if set to<br>
<i>true</i> will disable it. NOTE: the findbugs-maven-plugin itself <b>ignores</b> this configuration element.<br>
</p>
```
	  <plugin>
      <groupId>org.codehaus.mojo</groupId>
      <artifactId>findbugs-maven-plugin</artifactId>
      <version>2.3.1</version>
      <inherited>true</inherited>
      <configuration>
        <m2eclipseConfig>
          <disable>true</disable>
        </m2eclipseConfig>
      </configuration>
	  </plugin>

```