# JHipster on OpenShift

JHipster has a [beta OpenShift module](https://www.jhipster.tech/openshift/) for deploying JHipster applications to OpenShift clusters.

## Local Environment Setup

1. Install hypervisor (MacOS)
   ```
   brew install docker-machine-driver-xhyve
   sudo chown root:wheel /usr/local/opt/docker-machine-driver-xhyve/bin/docker-machine-driver-xhyve
   sudo chmod u+s /usr/local/opt/docker-machine-driver-xhyve/bin/docker-machine-driver-xhyve
   ```
1. Install [OpenShift Origin](https://github.com/openshift/origin/releases) or [OpenShift Container Platform](https://developers.redhat.com/products/cdk/overview/)

1. Install [MiniShift](https://docs.okd.io/latest/minishift/getting-started/installing.html#installing-with-homebrew)

## Generate an Application

1. Create a directory for your project
   ```
   mkdir jhipster-openshift
   cd jhipster-openshift
   ```

1. Generate a JHipster application

   ```
   $ jhipster
   ? Which *type* of application would you like to create? Monolithic application (recommended for simple projects)
   ? What is the base name of your application? openshipster
   ? What is your default Java package name? tech.ippon.opsnshipster
   ? Do you want to use the JHipster Registry to configure, monitor and scale your application? No
   ? Which *type* of authentication would you like to use? JWT authentication (stateless, with a token)
   ? Which *type* of database would you like to use? SQL (H2, MySQL, MariaDB, PostgreSQL, Oracle, MSSQL)
   ? Which *production* database would you like to use? MySQL
   ? Which *development* database would you like to use? H2 with disk-based persistence
   ? Do you want to use the Spring cache abstraction? Yes, with the Ehcache implementation (local cache, for a single node)
   ? Do you want to use Hibernate 2nd level cache? Yes
   ? Would you like to use Maven or Gradle for building the backend? Maven
   ? Which other technologies would you like to use? 
   ? Which *Framework* would you like to use for the client? React
   ? Would you like to enable *SASS* stylesheet preprocessor? No
   ? Would you like to enable internationalization support? No
   ? Besides JUnit and Jest, which testing frameworks would you like to use? 
   ? Would you like to install other generators from the JHipster Marketplace? (y/N) n
   ```

1. Run JHipster OpenShift sub-generator

   ```
   $ mkdir src/main/openshift
   $ cd src/main/openshift
   $ jhipster openshift
   INFO! Using JHipster version installed globally
   INFO! Executing jhipster:openshift
   INFO! Options: from-cli: true
   ⭕ [*BETA*] Welcome to the JHipster OpenShift Generator ⭕
   Files will be generated in folder: /Users/chrislumpkin/projects/jhipster-openshift or in the root directory path that you select in the subsequent step
   ✔ Docker is installed
   ? Which *type* of application would you like to deploy? (Use arrow keys)
   ❯ Monolithic application 
     Microservice application
   ```
