# User Guide #

## Requirements ##

  * A Maven2 project opened by m2eclipse.

## Rationale ##
<p>
The goal of m2e-extensions eclipse plugin is to read the maven plugin configuration from the pom.xml<br>
and configure the corresponding Eclipse plugin for the project. This allows to centralize the rulesets<br>
in one place which can configured in the Maven Project (pom.xml) as a plugin configuration. All maven<br>
enabled environmets (CI builds, Developer Environment(m2eclipse)) don't have to be configured explicitly.<br>
</p>

## FindBugs m2e-extensions Project Configurator ##

The findbugs project configurator documentation can be found [here](Findbugs.md).

## Checkstyle m2e-extensions Project Configurator ##

The checkstyle project configurator documentation can be found [here](Checkstyle.md).

## PMD m2e-extensions Project Configurator ##

The PMD project configurator documentation can be found [here](pmd.md).
