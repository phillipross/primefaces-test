![PrimeFaces icon](https://www.primefaces.org/wp-content/uploads/2016/10/prime_logo_new.png)

# PrimeFaces Test

This is a sample maven project that uses <strong>Latest PrimeFaces Release</strong> version. If you have a PrimeFaces issue, please download or fork this project. Then, you should change these files by yourself so that PrimeFaces Team can see your problem. Finally, you can send a link or attach the project. <strong>Please make sure that the project is runnable with the command below.</strong>

You can execute the sample against Jetty/OpenWebBeans with the `mvn jetty:run` maven command and navigate to <strong>http://localhost:8080/</strong> to access the page.

This project is configured to produce Java bytecode compatible with Java 11 and higher.  Java versions before Java 11 are no longer supported.

### JSF Versions
***

This maven project uses maven profiles to configure web container and JSF implementations/versions.  By default, the profiles for Jetty/OpenWebBeans and the Mojarra 2.3.x JSF implementations are enabled, but it is also possible to use other JSF implementations and versions with combinations of available maven profiles: jetty-owb, myfaces23, myfaces23next, mojarra23

`mvn clean jetty:run -Pjetty-owb,myfaces23`

`mvn clean jetty:run -Pjetty-owb,myfaces23next`

`mvn clean jetty:run -Pjetty-owb,mojarra23`

### Server Port
***

By default, the application runs on port 8080 but if you would like to use a different port you can pass `-Djetty.port=5000` like:

`mvn clean jetty:run -Djetty.port=5000`

### Jakarta EE10 Version
***

The branch `jakarta` contains a PrimeFaces Test setup to run again Jakarta EE10 profile using Jetty 11. You can also use other versions with the available maven profiles: mojarra40, myfaces40

`mvn clean jetty:run -Pmojarra40`

`mvn clean jetty:run -Pmyfaces40`

### JPA Lazy Datatable
***

The branch `jpa` contains a PrimeFaces Test setup to run with JPA using the JPA LazyDatatable advanced example.

### Visual Studio Code Quickstart
***

See the [quickstart guide for running in Visual Studio Code](./vscode-quickstart.md) for more information.

### Running with Payara
***

The branch `payara5` contains a PrimeFaces Test setup to run against a JavaEE/JakartaEE v8 profile using Payara v5 and the bundled Mojarra implementation of the Faces specification.  When using this setup, it is possible to use the `payara-micro:start` command and navigate to <strong>http://localhost:8080/</strong> to run the page.

`mvn clean install payara-micro:start -Ppayara5`

By default, the application runs on port 8080 but if you would like to use a different port you can pass `-Ddeploy.http.port=8765` like:

`mvn clean verify payara-micro:start -Ppayara5 -Ddeploy.http.port=8765`
