# Caravan AEM project

This is a project is use to manage the wcm-io Caravan files and dependencies. 
See the [GitHub Project](https://github.com/wcm-io-caravan/caravan-jaxrs).

## Modules
```
io.wcm.caravan.jaxrs.publisher - 1.2.0
io.wcm.osgi.wrapper.jersey - 2.27-0000
io.wcm.osgi.wrapper.hibernate-validator - 5.4.2-0000
javax.ws.rs-api - 2.1
validation-api - 1.1.0.Final
```

## Update version

Under `ui.apps` edit pom.xml dependencies. 

## How to build

To build all the modules run in the project root directory the following command with Maven 3:

    mvn clean install

If you have a running AEM instance you can build and package the whole project and deploy into AEM with  

    mvn clean install -PautoInstallPackage

Or to deploy it to a publish instance, run

    mvn clean install -PautoInstallPackagePublish

Or alternatively

    mvn clean install -PautoInstallPackage -Daem.port=4503

Or to deploy only the bundle to the author, run

    mvn clean install -PautoInstallBundle
