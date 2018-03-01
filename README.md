# kubernetes-service-catalog-client
This is a Java Client for Kubernetes Service Catalog access. Using this library you can list Service Brokers, Service Instances in a given Service Broker, Provision a Service, Bind to a Service. This library is incomplete in terms of creating Service Brokers and some other functions but could be easily added based on the need.

Mainly take look at the following classes and usage is trivial.
```
ServiceCatalogClient
ModelServiceCatalogClient
```
## Maven usage
```
<dependency>
  <groupId>org.teiid</groupId>
  <artifactId>kubernetes-service-catalog-client</artifactId>
  <version>0.0.3</version>
</dependency>
```

## How to do a release
```
git pull upstream master
mvn -DautoVersionSubmodules=true -P release clean package release:prepare
mvn -P release release:perform
```

Then goto https://oss.sonatype.org/#stagingRepositories to promote the jar to Maven Central
