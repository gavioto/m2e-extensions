# Introduction #

<p>
The m2e-extension Checkstyle project configurator will read the <i>maven-checkstyle-plugin</i> configuration<br>
from the pom.xml and configure the Eclipse-CS Plugin. Not, all <i>maven-checkstyle-plugin</i> are supported<br>
in the current release as some of these might not be applicable to the Eclipse-CS plugin.<br>
</p>

## CAVEATS ##
<p>
Remember if you are using the configurator (unless disabled) it will <b>override</b> any customization of<br>
the Eclipse-CS plugin. You should <b>not</b> use the m2e-extensions, if you would like to preserve your<br>
settings.<br>
</p>

## Supported maven-checkstyle-plugin elements ##

The following _maven-checkstyle-plugin_ configuration elments are supported:

  * _includes_
  * _configLocation_
  * _excludes_
  * _includeTestSourceDirectory_
  * _propertiesLocation_
  * _propertyExpansion_

## Disabling the configuration ##
<p>
The m2e-extension checkstyle project configurator can be disabled completely by adding the following<br>
configuration element. When you do this, the Eclipse-CS plugin will not be configured by the m2e-extensions<br>
project configurator. The element name is <i>m2eclipseConfig</i> and the child element <i>disable</i> if set to<br>
<i>true</i> will disable it. NOTE: the maven-checkstyle-plugin itself <b>ignores</b> this configuration element.<br>
</p>
```
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-checkstyle-plugin</artifactId>
        <version>2.4</version>
        <inherited>true</inherited>
        <configuration>
          <m2eclipseConfig>
          	<disable>true</disable>
          </m2eclipseConfig>
        </configuration>
      </plugin>

```