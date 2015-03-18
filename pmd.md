

# Introduction #

<p>
The m2e-extensions PMD project configurator will read the <i>maven-pmd-plugin</i> configuration<br>
from the pom.xml and configure the PMD Eclipse Plugin. Not, all <i>maven-pmd-plugin</i> are supported<br>
in the current release as some of these might not be applicable to the PMD Eclipse plugin.<br>
</p>

## CAVEATS ##
<p>
Remember if you are using the configurator (unless disabled) it will <b>override</b> any customization of<br>
the PMD Eclipse plugin. You should <b>not</b> use the m2e-extensions, if you would like to preserve your<br>
settings.<br>
</p>

## Supported maven-pmd-plugin elements ##

The following _maven-pmd-plugin_ configuration elments are supported:

  * _excludeRoots_
  * _excludes_
  * _includeTests_
  * _includes_
  * _rulesets_

## Disabling the configuration ##
<p>
The m2e-extension PMD project configurator can be disabled completely by adding the following<br>
configuration element. When you do this, the PMD Eclipse plugin will not be configured by the m2e-extensions<br>
project configurator. The element name is <i>m2eclipseConfig</i> and the child element <i>disable</i> if set to<br>
<i>true</i> will disable it. NOTE: the maven-pmd-plugin itself <b>ignores</b> this configuration element.<br>
</p>
```
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-pmd-plugin</artifactId>
        <version>2.4</version>
        <inherited>true</inherited>
        <configuration>
          <m2eclipseConfig>
          	<disable>true</disable>
          </m2eclipseConfig>
        </configuration>
      </plugin>

```