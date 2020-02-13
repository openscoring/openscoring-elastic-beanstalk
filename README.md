Openscoring-Elastic-Beanstalk
=============================

Openscoring application for the AWS Elastic Beanstalk orchestration service.

# Prerequisites #

* [EB CLI](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3.html).

# Installation #

Clone the repository:

```
git clone https://github.com/openscoring/openscoring-elastic-beanstalk.git
```

Enter the project root directory and edit the Openscoring application configuration file `.ebextensions/openscoring/application.conf` as necessary.
Download the latest [Openscoring webapp](https://repo1.maven.org/maven2/org/openscoring/openscoring-webapp/) WAR file from the Maven Central repository, and rename it to `ROOT.war`:

```
wget -O ROOT.war https://repo1.maven.org/maven2/org/openscoring/openscoring-webapp/2.0.1/openscoring-webapp-2.0.1.war
```

# Usage #

Initialize a local Elastic Beanstalk application configuration; use the `--platform` command-line option to specify `tomcat` platform type.

```
eb init --platform tomcat <application name>
```

Create a remote environment based on the local application configuration:

```
eb create
```

There should be a Model REST API endpoint ready at `http://<environment name>.<region>.elasticbeanstalk.com/model` now.

# License #

Openscoring-Elastic-Beanstalk is licensed under the terms and conditions of the [GNU Affero General Public License, Version 3.0](https://www.gnu.org/licenses/agpl-3.0.html).

# Additional information #

Openscoring-Elastic-Beanstalk is developed and maintained by Openscoring Ltd, Estonia.

Interested in using [Java PMML API](https://github.com/jpmml) or [Openscoring REST API](https://github.com/openscoring) software in your company? Please contact [info@openscoring.io](mailto:info@openscoring.io)