# WAR Plugin for Play framework 2.0

    Current version: 0.6

    Project-status: BETA
    
[![Build Status](https://play-war.ci.cloudbees.com/job/Play_2_War_-_on_push_-_with_integration_tests_-_on_develop_branch/badge/icon)](https://play-war.ci.cloudbees.com/job/Play_2_War_-_on_push_-_with_integration_tests_-_on_develop_branch/)

This project is a module for Play framework 2 to package your apps into standard WAR packages.

Live demo: JBoss7@Cloudbees : http://servlet30.play-war.cloudbees.net/

Other references built with Play 2 and Play2War:
 - [Factile](http://factile.net/) (Survey platform)

## Known limitations
* **Play2War is only compatible with Servlet 3.0 containers** (Tomcat 7, Jetty 8, JBoss 7, ...)
* **Play2War is only compatible with Java 6 JRE** (most of the application servers aren't compatible with too)
* **Your WAR must be deployed at root context** (sub-context deployment will be available with Play 2.1)
* As of version 0.6, it is only compatible with Play **2.0.2** (use Play2War v0.3 for Play 2.0 and v0.5 for Play 2.0.1)
 
## What's new ?

See [Changelog](/dlecan/play2-war-plugin/wiki/Changelog).

## Features
<table>
  <tr>
	<th rowspan="2" colspan="2">Feature</th>
    <th rowspan="2">Native Play 2</th>
	<th colspan="2">Servlet engine</th>
  </tr>
  <tr>
	<th>3.0</th>
	<th>2.4/2.5</th>
  </tr>
  <tr>
	<td colspan="2">Available ?</td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
    <td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
    <td>TBD</td>
  </tr>
  <tr>
	<td rowspan="4">HTTP</td>
    <td>Asynchronous request<br/>processing</td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161515/OK-2.png" height="20"></td>
  </tr>
  <tr>
    <td>GET/POST<br/>HTTP 1.0/1.1</td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
	<td>TBD</td>
  </tr>
  <tr>
    <td>Chunked response<br/>For long-polling</td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
	<td>TBD</td>
  </tr>
  <tr>
    <td>Web Socket</td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161515/OK-2.png" height="20"></td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161515/OK-2.png" height="20"></td>  
  </tr>
  <tr>
	<td rowspan="4">Container</td>
    <td>Data sources</td>
	<td>Built-in<br/>(<a href="http://jolbox.com/">Bone CP</a>)</td>
	<td colspan="2">Built-in (<a href="http://jolbox.com/">Bone CP</a>)<br/>External DS support : TBD</td>
  </tr>
  <tr>
    <td>Root context path
    <br/>Eg: http://local/</td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
	<td colspan="2"><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" title="WAR package must be deployed at root context" height="20"></td>
  </tr>
  <tr>
    <td>Non root context path
    <br/>Eg: http://local/myAppContext</td>
	<td>
        2.0.x : <img src="http://openclipart.org/image/800px/svg_to_png/161515/OK-2.png" height="20" title="Always deployed at root context">
        <br/>2.1.x (alpha) : <img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20">
    </td>
	<td colspan="2"><img src="http://openclipart.org/image/800px/svg_to_png/161515/OK-2.png" title="WAR package must be deployed at root context" height="20"><br/>TBD for Play 2.1</td>
  </tr>
  <tr>
    <td>WAR customization<br/>(web.xml, ...)</td>
	<td>N/A</td>
	<td>TBD</td>
	<td>TBD</td>  
  </tr>
</table>

## Server compatibility
<table>
  <tr>
	<th>Servlet engine</th>
    <th>Server</th>
	<th>Standalone deployment</th>
	<th>PaaS</th>
  </tr>
  <tr>
	<td rowspan="4">Servlet 3.0</td>
	<td>Tomcat 7</td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
  </tr>
  <tr>
	<td>JBoss 7.0</td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20">
		<a href="http://servlet30.play-war.cloudbees.net/" title="Play 2 WAR demo hosted at Cloudbees PaaS provider">Demo</a> @Cloudbees
		<br/><a href="https://github.com/dlecan/play2-war-plugin/wiki/FAQ#jboss7-deployment-at-cloudbees">Need extra configuration</a> when deploying
	</td>
  </tr>
  <tr>
	<td>JBoss 7.1</td>
	<td><img src="http://openclipart.org/image/800px/svg_to_png/161503/OK-1.png" height="20"></td>
	<td>TBD<br/>(Openshift)</td>
  </tr>
  <tr>
	<td>Glassfish 3</td>
	<td>TBD</td>
	<td>TBD</td>
  </tr>
  <tr>
	<td rowspan="2">Servlet 2.4/2.5</td>
	<td>Tomcat 6</td>
	<td>TBD</td>
	<td>TBD<br/>(Cloudbees)</td>
  </tr>
  <tr>
	<td>Jetty 6</td>
	<td>TBD</td>
	<td>TBD</td>
  </tr>
</table>

The plugin may work on others containers, such as Weblogic or Websphere (not tested yet).

## Usage

In the next descriptions, APP_HOME is the root of your Play 2.0 application you want to package as a WAR file.

### Add play2war plugin

In ``APP_HOME/project/plugins.sbt``, add:

```scala
resolvers += "Play2war plugins release" at "http://repository-play-war.forge.cloudbees.com/release/"

addSbtPlugin("com.github.play2war" % "play2-war-plugin" % "0.6")
```

### Add play2war runtime

In ``APP_HOME/project/Build.scala``, modify ``appDependencies`` and ``main`` values to add:

```scala
val appDependencies = Seq(
  ...
  "com.github.play2war" %% "play2-war-core" % "0.6"
  ...
)

val main = PlayProject(appName, appVersion, appDependencies, mainLang = SCALA).settings(
  ...
  resolvers += "Play2war plugins release" at "http://repository-play-war.forge.cloudbees.com/release/"
  ...
)
```

### Configure logging

You probably need to override default Play 2.0 logging configuration because:

- An external file will be written in ``$USER_HOME/logs/...``

- STDOUT appender pattern can be improved

Create a file ``APP_HOME/conf/logger.xml`` with the following content :

```xml
<configuration>
    
  <conversionRule conversionWord="coloredLevel" converterClass="play.api.Logger$ColoredLevel" />

  <appender name="STDOUT" class="ch.qos.logback.core.ConsoleAppender">
    <encoder>
      <pattern>%date - [%level] - from %logger in %thread %n%message%n%xException%n</pattern>
    </encoder>
  </appender>
  
  <logger name="play" level="INFO" />
  <logger name="application" level="INFO" />
  
  <!-- Off these ones as they are annoying, and anyway we manage configuration ourself -->
  <logger name="com.avaje.ebean.config.PropertyMapLoader" level="OFF" />
  <logger name="com.avaje.ebeaninternal.server.core.XmlConfigLoader" level="OFF" />
  <logger name="com.avaje.ebeaninternal.server.lib.BackgroundThread" level="OFF" />

  <root level="ERROR">
    <appender-ref ref="STDOUT" />
  </root>
```

**Warning: there is a known issue with JBoss and Play logger** (see [#54](/dlecan/play2-war-plugin/issues/54)).

</configuration>

## Packaging

If Play runtime is available, run

    play package

Your WAR package will be available in ``APP_HOME/target/<MY_PROJECT>_<YOUR_VERSION>.war``

## How to deploy in my favorite application server ?

**Play framework 2.0.x applications must be deployed at root context.**
Deployment in a sub-context is a known limitation which is fixed for Play 2.1 (still in development).

The best way to deploy at root context is to include a configuration file into the WAR file to indicate to your application server where to deploy the application.
But Play2War doesn't support file inclusion yet (see [#4](/dlecan/play2-war-plugin/issues/4)).

### How to deploy at root context in Tomcat 7

Rename the generated war *ROOT.war* before deployment.

### How to deploy at root context in Jetty 8

Rename the generated war *ROOT.war* before deployment.

### How to deploy at root context in JBoss 7.0.x

In ``standalone/configuration/standalone.xml``, comment the ``subsystem`` named ``urn:jboss:domain:pojo:1.0``.

Then follow explanations for JBoss 7.1.x below.

### How to deploy at root context in JBoss 7.1.x

First, disable default welcome page in ``standalone/configuration/standalone.xml`` by changing ``enable-welcome-root="true"`` to ``enable-welcome-root="false"``:

```xml
<subsystem xmlns="urn:jboss:domain:web:1.0" default-virtual-server="default-host">
  <connector name="http" scheme="http" protocol="HTTP/1.1" socket-binding="http"/>
  <virtual-server name="default-host" enable-welcome-root="true">
    <alias name="localhost" />
    <alias name="example.com" />
  </virtual-server>
</subsystem>
```

Then rename the generated war *ROOT.war* before deployment.

## Upload or deploy your WAR file

Upload or deploy your WAR file to your favorite Application Server if compatible (see <a href="#server-compatibility">Compatibility matrix above</a>).

## WAR publishing (Artifactory, Nexus, ...)

Play2war follows SBT rules, so built WAR can be published in a standard way (see [SBT Publish](https://github.com/harrah/xsbt/wiki/Publishing)).

## FAQ

See [FAQ](/dlecan/play2-war-plugin/wiki/FAQ).

## Issues

Please file issues here: https://github.com/dlecan/play2-war-plugin/issues.

## Continous integration

Watch it in action here : [https://play-war.ci.cloudbees.com/](https://play-war.ci.cloudbees.com/).

## How to help ?

Discover [how you can help the project](/dlecan/play2-war-plugin/wiki/How-to-help).

## Licence

This software is licensed under the Apache 2 license, quoted below.

Copyright 2012 Damien Lecan (http://www.dlecan.com).

Licensed under the Apache License, Version 2.0 (the "License"); you 
may not use this project except in compliance with the License. You 
may obtain a copy of the License at 

http://www.apache.org/licenses/LICENSE-2.0.

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Built by CloudBees
<img src="http://web-static-cloudfront.s3.amazonaws.com/images/badges/BuiltOnDEV.png"/>
